# Repo representing problem with protobuf library using google-cloud-platform library

## Using Python 3.12 everything is normal

## Using Python 3.13.0 there is error:

Traceback (most recent call last):
  File "/app/main.py", line 1, in <module>
    import vertexai
  File "/usr/local/lib/python3.13/site-packages/vertexai/__init__.py", line 19, in <module>
    from google.cloud.aiplatform import version as aiplatform_version
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform/__init__.py", line 24, in <module>
    from google.cloud.aiplatform import initializer
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform/initializer.py", line 35, in <module>
    from google.cloud.aiplatform import compat
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform/compat/__init__.py", line 18, in <module>
    from google.cloud.aiplatform.compat import services
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform/compat/services/__init__.py", line 18, in <module>
    from google.cloud.aiplatform_v1beta1.services.dataset_service import (
        client as dataset_service_client_v1beta1,
    )
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/__init__.py", line 21, in <module>
    from .services.dataset_service import DatasetServiceClient
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/services/dataset_service/__init__.py", line 16, in <module>
    from .client import DatasetServiceClient
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/services/dataset_service/client.py", line 53, in <module>
    from google.cloud.aiplatform_v1beta1.services.dataset_service import pagers
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/services/dataset_service/pagers.py", line 40, in <module>
    from google.cloud.aiplatform_v1beta1.types import annotation
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/types/__init__.py", line 31, in <module>
    from .batch_prediction_job import (
        BatchPredictionJob,
    )
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/types/batch_prediction_job.py", line 26, in <module>
    from google.cloud.aiplatform_v1beta1.types import explanation
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/types/explanation.py", line 22, in <module>
    from google.cloud.aiplatform_v1beta1.types import explanation_metadata
  File "/usr/local/lib/python3.13/site-packages/google/cloud/aiplatform_v1beta1/types/explanation_metadata.py", line 33, in <module>
    class ExplanationMetadata(proto.Message):
    ...<570 lines>...
        )
  File "/usr/local/lib/python3.13/site-packages/proto/message.py", line 279, in __new__
    file_info.generate_file_pb(new_class=cls, fallback_salt=full_name)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.13/site-packages/proto/_file_info.py", line 104, in generate_file_pb
    pool.Add(self.descriptor)
    ~~~~~~~~^^^^^^^^^^^^^^^^^
TypeError: Couldn't build proto file into descriptor pool: duplicate symbol 'google.cloud.aiplatform.v1beta1.ExplanationMetadata.InputMetadata.Visualization.__firstlineno__'
