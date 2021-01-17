---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479862"
---
# <span data-ttu-id="1b18b-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1b18b-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="1b18b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b18b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b18b-103">Frissíti a virtuális útválasztót.</span><span class="sxs-lookup"><span data-stu-id="1b18b-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="1b18b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b18b-104">SYNTAX</span></span>

### <span data-ttu-id="1b18b-105">VirtualRouterNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b18b-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b18b-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b18b-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b18b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b18b-107">DESCRIPTION</span></span>
<span data-ttu-id="1b18b-108">Frissíti a virtuális útválasztót az ág ág forgalmának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="1b18b-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="1b18b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b18b-109">EXAMPLES</span></span>

### <span data-ttu-id="1b18b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="1b18b-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="1b18b-111">Frissíti a virtuális útválasztót, hogy lehetővé tegye az ág ág forgalmát</span><span class="sxs-lookup"><span data-stu-id="1b18b-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="1b18b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1b18b-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="1b18b-113">A virtuális útválasztó frissítése az ág ág forgalmának blokkolása érdekében</span><span class="sxs-lookup"><span data-stu-id="1b18b-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="1b18b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b18b-114">PARAMETERS</span></span>

### <span data-ttu-id="1b18b-115">-AllowBranchToBrancTraffic</span><span class="sxs-lookup"><span data-stu-id="1b18b-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="1b18b-116">Flag to allow branch to branch traffic for virtual router.</span><span class="sxs-lookup"><span data-stu-id="1b18b-116">Flag to allow branch to branch traffic for virtual router.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b18b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b18b-117">-DefaultProfile</span></span>
<span data-ttu-id="1b18b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b18b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b18b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b18b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b18b-120">A virtuális útválasztó erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="1b18b-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b18b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b18b-121">-ResourceId</span></span>
<span data-ttu-id="1b18b-122">A virtuális útválasztó ResourceId-neve.</span><span class="sxs-lookup"><span data-stu-id="1b18b-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b18b-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="1b18b-123">-RouterName</span></span>
<span data-ttu-id="1b18b-124">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="1b18b-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b18b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b18b-125">CommonParameters</span></span>
<span data-ttu-id="1b18b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b18b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b18b-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b18b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b18b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b18b-128">INPUTS</span></span>

### <span data-ttu-id="1b18b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1b18b-129">System.String</span></span>

## <span data-ttu-id="1b18b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b18b-130">OUTPUTS</span></span>

### <span data-ttu-id="1b18b-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1b18b-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="1b18b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b18b-132">NOTES</span></span>

## <span data-ttu-id="1b18b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b18b-133">RELATED LINKS</span></span>
