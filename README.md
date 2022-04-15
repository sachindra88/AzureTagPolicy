# AzureTagPolicy
Inherit custom create 6 tags from resource group


Assign policy definitions for tag compliance

You use Azure Policy to enforce tagging rules and conventions. By creating a policy, you avoid the scenario of resources being deployed to your subscription that don't have the expected tags for your organization. Instead of manually applying tags or searching for resources that aren't compliant, you create a policy that automatically applies the needed tags during deployment. Tags can also now be applied to existing resources with the new Modify effect and a remediation task. The following section shows example policy definitions for tags.

<h2 id="policy-definitions">Policy definitions</h2>
<table>
<thead>
<tr>
<th>Name<br/><sub>(Azure portal)</sub></th>
<th>Description</th>
<th>Effect(s)</th>
<th>Version<br/><sub>(GitHub)</sub></th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F726aca4c-86e9-4b04-b0c5-073027359532" data-linktype="external">Add a tag to resource groups</a></td>
<td>Adds the specified tag and value when any resource group missing this tag is created or updated. Existing resource groups can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddTag_ResourceGroup_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F4f9dc7db-30c1-420c-b61a-e1d640128d26" data-linktype="external">Add a tag to resources</a></td>
<td>Adds the specified tag and value when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed. Does not modify tags on resource groups.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddTag_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F96d9a89c-0d67-41fc-899d-2b9599f76a24" data-linktype="external">Add a tag to subscriptions</a></td>
<td>Adds the specified tag and value to subscriptions via a remediation task. If the tag exists with a different value it will not be changed. See <a href="../../governance/policy/how-to/remediate-resources" data-linktype="relative-path">https://aka.ms/azurepolicyremediation</a> for more information on policy remediation.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddTag_Subscription_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fd157c373-a6c4-483d-aaad-570756956268" data-linktype="external">Add or replace a tag on resource groups</a></td>
<td>Adds or replaces the specified tag and value when any resource group is created or updated. Existing resource groups can be remediated by triggering a remediation task.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddOrReplaceTag_ResourceGroup_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F5ffd78d9-436d-4b41-a421-5baa819e3008" data-linktype="external">Add or replace a tag on resources</a></td>
<td>Adds or replaces the specified tag and value when any resource is created or updated. Existing resources can be remediated by triggering a remediation task. Does not modify tags on resource groups.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddOrReplaceTag_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F61a4d60b-7326-440e-8051-9f94394d4dd1" data-linktype="external">Add or replace a tag on subscriptions</a></td>
<td>Adds or replaces the specified tag and value on subscriptions via a remediation task. Existing resource groups can be remediated by triggering a remediation task. See <a href="../../governance/policy/how-to/remediate-resources" data-linktype="relative-path">https://aka.ms/azurepolicyremediation</a> for more information on policy remediation.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddOrReplaceTag_Subscription_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F9ea02ca2-71db-412d-8b00-7c7ca9fcd32d" data-linktype="external">Append a tag and its value from the resource group</a></td>
<td>Appends the specified tag with its value from the resource group when any resource which is missing this tag is created or updated. Does not modify the tags of resources created before this policy was applied until those resources are changed. New 'modify' effect policies are available that support remediation of tags on existing resources (see <a href="/en-us/azure/governance/policy/concepts/effects#modify" data-linktype="absolute-path">https://aka.ms/modifydoc</a>).</td>
<td>append</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Append.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" data-linktype="external">Append a tag and its value to resource groups</a></td>
<td>Appends the specified tag and value when any resource group which is missing this tag is created or updated. Does not modify the tags of resource groups created before this policy was applied until those resource groups are changed. New 'modify' effect policies are available that support remediation of tags on existing resources (see <a href="/en-us/azure/governance/policy/concepts/effects#modify" data-linktype="absolute-path">https://aka.ms/modifydoc</a>).</td>
<td>append</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ResourceGroupApplyTag_Append.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F2a0e14a6-b0a6-4fab-991a-187a4f81c498" data-linktype="external">Append a tag and its value to resources</a></td>
<td>Appends the specified tag and value when any resource which is missing this tag is created or updated. Does not modify the tags of resources created before this policy was applied until those resources are changed. Does not apply to resource groups. New 'modify' effect policies are available that support remediation of tags on existing resources (see <a href="/en-us/azure/governance/policy/concepts/effects#modify" data-linktype="absolute-path">https://aka.ms/modifydoc</a>).</td>
<td>append</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ApplyTag_Append.json" data-linktype="external">1.0.1</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fcd3aa116-8754-49c9-a813-ad46512ece54" data-linktype="external">Inherit a tag from the resource group</a></td>
<td>Adds or replaces the specified tag and value from the parent resource group when any resource is created or updated. Existing resources can be remediated by triggering a remediation task.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_AddOrReplace_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fea3f2387-9b95-492a-a190-fcdc54f7b070" data-linktype="external">Inherit a tag from the resource group if missing</a></td>
<td>Adds the specified tag with its value from the parent resource group when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Add_Modify.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fb27a0cbd-a167-4dfa-ae64-4337be671140" data-linktype="external">Inherit a tag from the subscription</a></td>
<td>Adds or replaces the specified tag and value from the containing subscription when any resource is created or updated. Existing resources can be remediated by triggering a remediation task.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_AddOrReplace_FromSubscription.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F40df99da-1232-49b1-a39a-6da8d878f469" data-linktype="external">Inherit a tag from the subscription if missing</a></td>
<td>Adds the specified tag with its value from the containing subscription when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed.</td>
<td>modify</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Add_FromSubscription.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F8ce3da23-7156-49e4-b145-24f95f9dcb46" data-linktype="external">Require a tag and its value on resource groups</a></td>
<td>Enforces a required tag and its value on resource groups.</td>
<td>deny</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ResourceGroupRequireTagAndValue_Deny.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F1e30110a-5ceb-460c-a204-c1c3969c6d62" data-linktype="external">Require a tag and its value on resources</a></td>
<td>Enforces a required tag and its value. Does not apply to resource groups.</td>
<td>deny</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/RequireTagAndValue_Deny.json" data-linktype="external">1.0.1</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F96670d01-0a4d-4649-9c89-2d3abc0a5025" data-linktype="external">Require a tag on resource groups</a></td>
<td>Enforces existence of a tag on resource groups.</td>
<td>deny</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ResourceGroupRequireTag_Deny.json" data-linktype="external">1.0.0</a></td>
</tr>
<tr>
<td><a href="https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F871b6d14-10aa-478d-b590-94f262ecfa99" data-linktype="external">Require a tag on resources</a></td>
<td>Enforces existence of a tag. Does not apply to resource groups.</td>
<td>deny</td>
<td><a href="https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/RequireTag_Deny.json" data-linktype="external">1.0.1</a></td>
</tr>
</tbody>
</table>
<h2 id="next-steps">Next steps</h2>
<ul>
<li>To learn about tagging resources, see <a href="tag-resources" data-linktype="relative-path">Use tags to organize your Azure resources</a>.</li>
<li>Not all resource types support tags. To determine if you can apply a tag to a resource type, see <a href="tag-support" data-linktype="relative-path">Tag support for Azure resources</a>.</li>
</ul>
