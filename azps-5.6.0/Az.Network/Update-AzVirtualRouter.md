---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: 119dec74416b8447d04aef7ae101016490408b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918401"
---
# <span data-ttu-id="b694e-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b694e-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="b694e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b694e-102">SYNOPSIS</span></span>
<span data-ttu-id="b694e-103">Frissíti a virtuális útválasztót.</span><span class="sxs-lookup"><span data-stu-id="b694e-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="b694e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b694e-104">SYNTAX</span></span>

### <span data-ttu-id="b694e-105">VirtualRouterNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b694e-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b694e-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b694e-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b694e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b694e-107">DESCRIPTION</span></span>
<span data-ttu-id="b694e-108">Frissíti a virtuális útválasztót az ág ág forgalmának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="b694e-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="b694e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b694e-109">EXAMPLES</span></span>

### <span data-ttu-id="b694e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b694e-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="b694e-111">Frissíti a virtuális útválasztót, hogy lehetővé tegye az ág ág forgalmát</span><span class="sxs-lookup"><span data-stu-id="b694e-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="b694e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="b694e-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="b694e-113">A virtuális útválasztó frissítése elágaztatási forgalom blokkolása érdekében</span><span class="sxs-lookup"><span data-stu-id="b694e-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="b694e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b694e-114">PARAMETERS</span></span>

### <span data-ttu-id="b694e-115">-AllowBranchToBrancTraffic</span><span class="sxs-lookup"><span data-stu-id="b694e-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="b694e-116">Flag to allow branch to branch traffic for virtual router.</span><span class="sxs-lookup"><span data-stu-id="b694e-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="b694e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b694e-117">-DefaultProfile</span></span>
<span data-ttu-id="b694e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b694e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b694e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b694e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b694e-120">A virtuális útválasztó erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="b694e-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="b694e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b694e-121">-ResourceId</span></span>
<span data-ttu-id="b694e-122">A virtuális útválasztó ResourceId-neve.</span><span class="sxs-lookup"><span data-stu-id="b694e-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="b694e-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="b694e-123">-RouterName</span></span>
<span data-ttu-id="b694e-124">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="b694e-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="b694e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b694e-125">CommonParameters</span></span>
<span data-ttu-id="b694e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b694e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b694e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b694e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b694e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b694e-128">INPUTS</span></span>

### <span data-ttu-id="b694e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b694e-129">System.String</span></span>

## <span data-ttu-id="b694e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b694e-130">OUTPUTS</span></span>

### <span data-ttu-id="b694e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b694e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="b694e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b694e-132">NOTES</span></span>

## <span data-ttu-id="b694e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b694e-133">RELATED LINKS</span></span>
