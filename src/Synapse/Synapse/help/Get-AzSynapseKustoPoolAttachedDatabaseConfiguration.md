---
external help file:
Module Name: Az.Synapse
online version: https://learn.microsoft.com/powershell/module/az.synapse/get-azsynapsekustopoolattacheddatabaseconfiguration
schema: 2.0.0
---

# Get-AzSynapseKustoPoolAttachedDatabaseConfiguration

## SYNOPSIS
Returns an attached database configuration.

## SYNTAX

### List (Default)
```
Get-AzSynapseKustoPoolAttachedDatabaseConfiguration -KustoPoolName <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Get
```
Get-AzSynapseKustoPoolAttachedDatabaseConfiguration -AttachedDatabaseConfigurationName <String>
 -KustoPoolName <String> -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzSynapseKustoPoolAttachedDatabaseConfiguration -InputObject <ISynapseIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Returns an attached database configuration.

## EXAMPLES

### Example 1: List all the AttachedDatabaseConfigurations in a kusto pool
```powershell
Get-AzSynapseKustoPoolAttachedDatabaseConfiguration -ResourceGroupName testrg -WorkspaceName testws -KustoPoolName testfollowerkustopool
```

```output
Name                                               Type                                                                   Location
----                                               ----                                                                   --------
testws/testfollowerkustopool/followerconfiguration Microsoft.Synapse/workspaces/kustoPools/AttachedDatabaseConfigurations East US 2
```

The above command lists all the AttachedDatabaseConfigurations in the kusto pool "testfollowerkustopool".

### Example 2: Get a specific AttachedDatabaseConfiguration in a kusto pool
```powershell
Get-AzSynapseKustoPoolAttachedDatabaseConfiguration -ResourceGroupName testrg -WorkspaceName testws -KustoPoolName testfollowerkustopool -Name followerconfiguration
```

```output
Name                                               Type                                                                   Location
----                                               ----                                                                   --------
testws/testfollowerkustopool/followerconfiguration Microsoft.Synapse/workspaces/kustoPools/AttachedDatabaseConfigurations East US 2
```

The above command returns the AttachedDatabaseConfigurations named "followerconfiguration" in the cluster "testfollowerkustopool".

## PARAMETERS

### -AttachedDatabaseConfigurationName
The name of the attached database configuration.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Synapse.Models.ISynapseIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KustoPoolName
The name of the Kusto pool.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group.
The name is case insensitive.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
The ID of the target subscription.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
The name of the workspace

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Synapse.Models.ISynapseIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Synapse.Models.Api20210601Preview.IAttachedDatabaseConfiguration

## NOTES

ALIASES

COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.


INPUTOBJECT `<ISynapseIdentity>`: Identity Parameter
  - `[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.
  - `[DataConnectionName <String>]`: The name of the data connection.
  - `[DatabaseName <String>]`: The name of the database in the Kusto pool.
  - `[Id <String>]`: Resource identity path
  - `[KustoPoolName <String>]`: The name of the Kusto pool.
  - `[Location <String>]`: The name of Azure region.
  - `[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.
  - `[ResourceGroupName <String>]`: The name of the resource group. The name is case insensitive.
  - `[SubscriptionId <String>]`: The ID of the target subscription.
  - `[WorkspaceName <String>]`: The name of the workspace

## RELATED LINKS

