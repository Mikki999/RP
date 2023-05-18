 * Generates a random password
 *
 * @param {number} length - The length of the password
 * @returns {string} - The generated password
 */
function generateRandomPassword(length) {
    // Check if length is a number
    if (typeof length !== 'number') {
        throw new Error('Length must be a number');
    }

    // Check if length is greater than 0
    if (length <= 0) {
        throw new Error('Length must be greater than 0');
    }

    // Create an array of characters to use
    const characters = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()_+-=';

    // Create an empty string to store the password
    let password = '';

    // Generate the password
    for (let i = 0; i < length; i++) {
        // Get a random index from the characters array
        const randomIndex = Math.floor(Math.random() * characters.length);

        // Add the character to the password
        password += characters[randomIndex];
    }

    // Return the generated password
    return password;
}
