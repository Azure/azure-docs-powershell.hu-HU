---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209951"
---
# <span data-ttu-id="ffc04-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-101">Update-AzContainerService</span></span>

## <span data-ttu-id="ffc04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc04-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc04-103">Frissíti egy tárolószolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="ffc04-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="ffc04-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ffc04-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc04-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ffc04-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc04-106">Az **Update-AzContainerService** parancsmag frissíti egy tárolószolgáltatás állapotát úgy, hogy megfeleljen a szolgáltatás helyi példányának.</span><span class="sxs-lookup"><span data-stu-id="ffc04-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="ffc04-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ffc04-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc04-108">1. példa: Tárolószolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="ffc04-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="ffc04-109">Ez a parancs a CSResourceGroup17 nevű tárolószolgáltatást a Get-AzContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffc04-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="ffc04-110">A parancs a folyamat műveleti Remove-AzContainerServiceAgentPoolProfile átadja az objektumot a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ffc04-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ffc04-111">**A Remove-AzContainerServiceAgentPoolProfile** eltávolítja az AgentPool01 nevű profilt.</span><span class="sxs-lookup"><span data-stu-id="ffc04-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="ffc04-112">A parancs átadja az eredményt a Add-AzContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ffc04-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="ffc04-113">**Az Add-AzContainerServiceAgentPoolProfile** hozzáad egy AgentPool01 nevű profilt, és rendelkezik a megadott tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="ffc04-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="ffc04-114">A parancs átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="ffc04-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="ffc04-115">Az aktuális parancsmag frissíti a tárolószolgáltatást, hogy tükrözze az ebben a parancsban végrehajtott módosításokat.</span><span class="sxs-lookup"><span data-stu-id="ffc04-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="ffc04-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffc04-116">PARAMETERS</span></span>

### <span data-ttu-id="ffc04-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffc04-117">-AsJob</span></span>
<span data-ttu-id="ffc04-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ffc04-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc04-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-119">-ContainerService</span></span>
<span data-ttu-id="ffc04-120">Egy módosításokat tartalmazó **helyi ContainerService-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="ffc04-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc04-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc04-121">-DefaultProfile</span></span>
<span data-ttu-id="ffc04-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffc04-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc04-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ffc04-123">-Name</span></span>
<span data-ttu-id="ffc04-124">A parancsmag által frissülő tárolószolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffc04-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc04-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc04-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffc04-126">A parancsmag által frissülő tárolószolgáltatás erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffc04-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc04-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffc04-127">-Confirm</span></span>
<span data-ttu-id="ffc04-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ffc04-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc04-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc04-129">-WhatIf</span></span>
<span data-ttu-id="ffc04-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ffc04-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc04-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffc04-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc04-132">CommonParameters</span></span>
<span data-ttu-id="ffc04-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc04-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffc04-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc04-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffc04-135">INPUTS</span></span>

### <span data-ttu-id="ffc04-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc04-136">System.String</span></span>

### <span data-ttu-id="ffc04-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ffc04-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffc04-138">OUTPUTS</span></span>

### <span data-ttu-id="ffc04-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ffc04-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ffc04-140">NOTES</span></span>

## <span data-ttu-id="ffc04-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffc04-141">RELATED LINKS</span></span>

[<span data-ttu-id="ffc04-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="ffc04-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="ffc04-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="ffc04-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="ffc04-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="ffc04-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="ffc04-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="ffc04-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


