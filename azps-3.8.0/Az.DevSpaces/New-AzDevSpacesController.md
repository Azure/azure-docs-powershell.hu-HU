---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014358"
---
# <span data-ttu-id="d0fe1-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="d0fe1-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="d0fe1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fe1-103">Hozzon létre egy új Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="d0fe1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0fe1-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0fe1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0fe1-105">DESCRIPTION</span></span>
<span data-ttu-id="d0fe1-106">Hozzon létre egy új Azure DevSpaces-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="d0fe1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0fe1-107">EXAMPLES</span></span>

### <span data-ttu-id="d0fe1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0fe1-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="d0fe1-109">Hozzon létre egy DevSpaces-vezérlőt a resourcegroup devSpaceResourceGroup nevű devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="d0fe1-110">Használja a fürtnév-fürtöt a vezérlő céljaihoz.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="d0fe1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0fe1-111">PARAMETERS</span></span>

### <span data-ttu-id="d0fe1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0fe1-112">-AsJob</span></span>
<span data-ttu-id="d0fe1-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d0fe1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0fe1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0fe1-114">-DefaultProfile</span></span>
<span data-ttu-id="d0fe1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0fe1-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0fe1-116">-Name</span></span>
<span data-ttu-id="d0fe1-117">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="d0fe1-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fe1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0fe1-118">-ResourceGroupName</span></span>
<span data-ttu-id="d0fe1-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fe1-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="d0fe1-120">-Tag</span></span>
<span data-ttu-id="d0fe1-121">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fe1-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="d0fe1-122">-TargetClusterName</span></span>
<span data-ttu-id="d0fe1-123">A cél fürtjének neve.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fe1-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0fe1-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="d0fe1-125">Cél erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fe1-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0fe1-126">-Confirm</span></span>
<span data-ttu-id="d0fe1-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0fe1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0fe1-128">-WhatIf</span></span>
<span data-ttu-id="d0fe1-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0fe1-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0fe1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0fe1-131">CommonParameters</span></span>
<span data-ttu-id="d0fe1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0fe1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0fe1-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0fe1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0fe1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0fe1-134">INPUTS</span></span>

### <span data-ttu-id="d0fe1-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="d0fe1-135">None</span></span>

## <span data-ttu-id="d0fe1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0fe1-136">OUTPUTS</span></span>

### <span data-ttu-id="d0fe1-137">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="d0fe1-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="d0fe1-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0fe1-138">NOTES</span></span>

## <span data-ttu-id="d0fe1-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0fe1-139">RELATED LINKS</span></span>
