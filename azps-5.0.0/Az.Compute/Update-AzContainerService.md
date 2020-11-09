---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296447"
---
# <span data-ttu-id="55a08-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-101">Update-AzContainerService</span></span>

## <span data-ttu-id="55a08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55a08-102">SYNOPSIS</span></span>
<span data-ttu-id="55a08-103">Frissíti a tároló szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="55a08-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="55a08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55a08-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a08-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55a08-105">DESCRIPTION</span></span>
<span data-ttu-id="55a08-106">Az **Update-AzContainerService** parancsmag frissíti a tároló szolgáltatás állapotát a szolgáltatás helyi példányának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="55a08-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="55a08-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55a08-107">EXAMPLES</span></span>

### <span data-ttu-id="55a08-108">Példa 1: tároló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="55a08-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="55a08-109">Ez a parancs a CSResourceGroup17 nevű tároló szolgáltatást az Get-AzContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="55a08-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="55a08-110">A parancs a pipeline operátor segítségével átadja az objektumot az Remove-AzContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="55a08-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="55a08-111">**Remove-AzContainerServiceAgentPoolProfile –** eltávolítja a AgentPool01 nevű profilt.</span><span class="sxs-lookup"><span data-stu-id="55a08-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="55a08-112">A parancs átadja az eredményt az Add-AzContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="55a08-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="55a08-113">A **Add-AzContainerServiceAgentPoolProfile** felveszi a AgentPool01 nevű profilt, és a megadott tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="55a08-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="55a08-114">A parancs átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="55a08-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="55a08-115">Az aktuális parancsmag frissíti a tároló szolgáltatást a parancsban elvégzett módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="55a08-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="55a08-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55a08-116">PARAMETERS</span></span>

### <span data-ttu-id="55a08-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a08-117">-AsJob</span></span>
<span data-ttu-id="55a08-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="55a08-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a08-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-119">-ContainerService</span></span>
<span data-ttu-id="55a08-120">Egy olyan helyi **ContainerService** -objektumot ad meg, amely módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="55a08-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="55a08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a08-121">-DefaultProfile</span></span>
<span data-ttu-id="55a08-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55a08-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55a08-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55a08-123">-Name</span></span>
<span data-ttu-id="55a08-124">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag frissíti.</span><span class="sxs-lookup"><span data-stu-id="55a08-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="55a08-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a08-125">-ResourceGroupName</span></span>
<span data-ttu-id="55a08-126">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="55a08-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="55a08-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55a08-127">-Confirm</span></span>
<span data-ttu-id="55a08-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55a08-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a08-129">-WhatIf</span></span>
<span data-ttu-id="55a08-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="55a08-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a08-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55a08-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a08-132">CommonParameters</span></span>
<span data-ttu-id="55a08-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55a08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a08-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="55a08-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a08-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55a08-135">INPUTS</span></span>

### <span data-ttu-id="55a08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="55a08-136">System.String</span></span>

### <span data-ttu-id="55a08-137">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="55a08-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55a08-138">OUTPUTS</span></span>

### <span data-ttu-id="55a08-139">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="55a08-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55a08-140">NOTES</span></span>

## <span data-ttu-id="55a08-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55a08-141">RELATED LINKS</span></span>

[<span data-ttu-id="55a08-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="55a08-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="55a08-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="55a08-144">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="55a08-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="55a08-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="55a08-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="55a08-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


