---
sidebar_position: 8
description: Action result object is the result of an action execution.
---

# Action result object

Here's how action result object is structured (all keys are optional):

- `data`: when execution is successful, what you returned in action's server code.
- `validationErrors`: when input data doesn't pass validation, an object that contains the validation errors. Can be customized using [`defaultValidationErrorsShape`](/docs/define-actions/create-the-client#defaultvalidationerrorsshape) initialization option and/or via [`handleValidationErrorsShape`function passed to `schema` method](/docs/define-actions/validation-errors#customize-validation-errors-format).
- `bindArgsValidationErrors`: when bound arguments don't pass validation, an object that contains the validation errors. Can be customized using [`defaultValidationErrorsShape`](/docs/define-actions/create-the-client#defaultvalidationerrorsshape) initialization option and/or via [`handleBindArgsValidationErrorsShape` function passed to `bindArgsSchemas` method](/docs/define-actions/validation-errors#customize-validation-errors-format).
- `serverError`: when execution fails, an error object that contains the error message, customizable by using the [`handleReturnedServerError`](/docs/define-actions/create-the-client#handlereturnedservererror) initialization function.