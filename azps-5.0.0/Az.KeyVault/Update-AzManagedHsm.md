---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195897"
---
# <span data-ttu-id="eadfa-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="eadfa-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="eadfa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eadfa-102">SYNOPSIS</span></span>
<span data-ttu-id="eadfa-103">Frissítse az Azure Managed HSM állapotát.</span><span class="sxs-lookup"><span data-stu-id="eadfa-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="eadfa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eadfa-104">SYNTAX</span></span>

### <span data-ttu-id="eadfa-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eadfa-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadfa-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadfa-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadfa-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadfa-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eadfa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eadfa-108">DESCRIPTION</span></span>
<span data-ttu-id="eadfa-109">Ez a parancsmag frissíti az Azure Managed HSM állapotát.</span><span class="sxs-lookup"><span data-stu-id="eadfa-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="eadfa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eadfa-110">EXAMPLES</span></span>

### <span data-ttu-id="eadfa-111">1. példa: a felügyelt HSM közvetlen frissítése</span><span class="sxs-lookup"><span data-stu-id="eadfa-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

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

<span data-ttu-id="eadfa-112">Frissíti az erőforráscsoport nevű felügyelt HSM címkéit `$hsmName` `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="eadfa-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="eadfa-113">2. példa: a felügyelt HSM frissítése csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="eadfa-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="eadfa-114">Frissíti a felügyelt HSM címkéit a csőhálózat-szintaxis használatával.</span><span class="sxs-lookup"><span data-stu-id="eadfa-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="eadfa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eadfa-115">PARAMETERS</span></span>

### <span data-ttu-id="eadfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadfa-116">-DefaultProfile</span></span>
<span data-ttu-id="eadfa-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eadfa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eadfa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eadfa-118">-InputObject</span></span>
<span data-ttu-id="eadfa-119">Felügyelt HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="eadfa-119">Managed HSM object.</span></span>

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

### <span data-ttu-id="eadfa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eadfa-120">-Name</span></span>
<span data-ttu-id="eadfa-121">A felügyelt HSM neve</span><span class="sxs-lookup"><span data-stu-id="eadfa-121">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="eadfa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eadfa-122">-ResourceGroupName</span></span>
<span data-ttu-id="eadfa-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eadfa-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="eadfa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eadfa-124">-ResourceId</span></span>
<span data-ttu-id="eadfa-125">A felügyelt HSM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eadfa-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="eadfa-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="eadfa-126">-Tag</span></span>
<span data-ttu-id="eadfa-127">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="eadfa-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="eadfa-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eadfa-128">-Confirm</span></span>
<span data-ttu-id="eadfa-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eadfa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eadfa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eadfa-130">-WhatIf</span></span>
<span data-ttu-id="eadfa-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eadfa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eadfa-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eadfa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eadfa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadfa-133">CommonParameters</span></span>
<span data-ttu-id="eadfa-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eadfa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadfa-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eadfa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadfa-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eadfa-136">INPUTS</span></span>

### <span data-ttu-id="eadfa-137">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="eadfa-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="eadfa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eadfa-138">System.String</span></span>

### <span data-ttu-id="eadfa-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eadfa-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eadfa-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eadfa-140">OUTPUTS</span></span>

### <span data-ttu-id="eadfa-141">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="eadfa-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="eadfa-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eadfa-142">NOTES</span></span>

## <span data-ttu-id="eadfa-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eadfa-143">RELATED LINKS</span></span>

[<span data-ttu-id="eadfa-144">Új – AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="eadfa-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="eadfa-145">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="eadfa-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="eadfa-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="eadfa-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)