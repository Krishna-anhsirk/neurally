# Neurally Guide

## How to run Neurally locally

1. Clone the repo locally.
2. Navigate to the Neurally folder: `cd Neurally`
3. Install dependencies: `npm install`
4. Navigate to the scripts directory: `cd src/scripts`
5. **Note:** Commands may vary by OS. Search online if needed.
6. Create a virtual environment: `python -m venv venv`
7. Activate the virtual environment: `venv\Scripts\activate`
8. Install Python dependencies: `pip install -r requirements.txt`
9. Return to the root project: `cd ../..`
10. Run in development mode: `npm run dev`

## How to Add a New Feature for a Test Type

1. **Add the new feature to the Python files** for the desired test type.

2. **Add the feature details to `featuresData.js`.**  
   - The key must match exactly with the feature name in the Python files.  
   - Define the properties: `title`, `description`, and `units`.

   Example:

   ```javascript
   shimmer_DDA: { // Must match the feature name from the Python files
       // These properties are displayed in the UI
       title: 'Shimmer DDA',
       description: 'Shimmer is very important',
       units: 'dimensionless'
   }
   ```

3. **Add the feature name to `TEST_FEATURE_LIST, featuresData.js`.**  
    -  Add the key of the feature to the test feature list.

    ```javascript
    export const TEST_FEATURE_LIST = [
        'existingFeature',
        'existingFeature',
        'existingFeature',
        'shimmer_DDA' // Newly feature added
    ];
    ```

4. This will add the new feature to the test type.
