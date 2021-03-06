.. Copyright 2010-2016 Amazon.com, Inc. or its affiliates. All Rights Reserved.

   This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0
   International License (the "License"). You may not use this file except in compliance with the
   License. A copy of the License is located at http://creativecommons.org/licenses/by-nc-sa/4.0/.

   This file is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
   either express or implied. See the License for the specific language governing permissions and
   limitations under the License.

###################
Registering Domains
###################

Every workflow and activity in |SWF|_ needs a :emphasis:`domain` to run in.

**To register an Amazon SWF domain**

1.  Create a new :java-api:`RegisterDomainRequest
    <services/simpleworkflow/model/RegisterDomainRequest>` object, providing it with at least the
    domain name and workflow execution retention period (these parameters are both required).

2.  Call the :java-ref:`AmazonSimpleWorkflowClient.registerDomain
    </services/simpleworkflow/AmazonSimpleWorkflowClient.html#registerDomain(com.amazonaws.services.simpleworkflow.model.RegisterDomainRequest)>`
    method with the :emphasis:`RegisterDomainRequest` object.

3.  Catch the :java-api:`DomainAlreadyExistsException
    <services/simpleworkflow/model/DomainAlreadyExistsException>` if the domain you're requesting
    already exists (in which case, no action is usually required).

The following code demonstrates this procedure:

.. literalinclude:: snippets/CreateSwfDomain-register_swf_domain.java
    :language: java
    :lines: 14-

