---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152618"
---
# <span data-ttu-id="8e5ec-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="8e5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5ec-103">Frissítse egy Azure által felügyelt HSM állapotát.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="8e5ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e5ec-104">SYNTAX</span></span>

### <span data-ttu-id="8e5ec-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e5ec-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e5ec-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e5ec-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e5ec-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e5ec-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e5ec-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e5ec-108">DESCRIPTION</span></span>
<span data-ttu-id="8e5ec-109">Ez a parancsmag frissíti egy Azure által felügyelt HSM állapotát.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="8e5ec-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e5ec-110">EXAMPLES</span></span>

### <span data-ttu-id="8e5ec-111">1. példa: Felügyelt Hsm frissítése közvetlenül</span><span class="sxs-lookup"><span data-stu-id="8e5ec-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="8e5ec-112">Frissíti az erőforráscsoportban elnevezett felügyelt Hsm `$hsmName` `$resourceGroupName` címkéit.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="8e5ec-113">2. példa: Felügyelt Hsm frissítése pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="8e5ec-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="8e5ec-114">A felügyelt HSM címkéit pipázási szintaxissal frissíti.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="8e5ec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e5ec-115">PARAMETERS</span></span>

### <span data-ttu-id="8e5ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5ec-116">-DefaultProfile</span></span>
<span data-ttu-id="8e5ec-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e5ec-118">-InputObject</span></span>
<span data-ttu-id="8e5ec-119">Felügyelt HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8e5ec-120">-Name</span></span>
<span data-ttu-id="8e5ec-121">A felügyelt HSM neve.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e5ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e5ec-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e5ec-124">-ResourceId</span></span>
<span data-ttu-id="8e5ec-125">A felügyelt HSM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e5ec-126">-Tag</span></span>
<span data-ttu-id="8e5ec-127">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-128">-Confirm</span></span>
<span data-ttu-id="8e5ec-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5ec-130">-WhatIf</span></span>
<span data-ttu-id="8e5ec-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e5ec-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5ec-133">CommonParameters</span></span>
<span data-ttu-id="8e5ec-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5ec-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e5ec-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5ec-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e5ec-136">INPUTS</span></span>

### <span data-ttu-id="8e5ec-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="8e5ec-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8e5ec-138">System.String</span></span>

### <span data-ttu-id="8e5ec-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e5ec-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8e5ec-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e5ec-140">OUTPUTS</span></span>

### <span data-ttu-id="8e5ec-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="8e5ec-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e5ec-142">NOTES</span></span>

## <span data-ttu-id="8e5ec-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e5ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e5ec-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="8e5ec-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="8e5ec-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8e5ec-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)