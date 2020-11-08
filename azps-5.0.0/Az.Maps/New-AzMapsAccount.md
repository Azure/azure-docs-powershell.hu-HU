---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195814"
---
# <span data-ttu-id="629c4-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="629c4-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="629c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="629c4-102">SYNOPSIS</span></span>
<span data-ttu-id="629c4-103">Azure Maps-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="629c4-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="629c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="629c4-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="629c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="629c4-105">DESCRIPTION</span></span>
<span data-ttu-id="629c4-106">Az New-AzMapsAccount parancsmag létrehoz egy Azure Maps-fiókot a megadott SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="629c4-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="629c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="629c4-107">EXAMPLES</span></span>

### <span data-ttu-id="629c4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="629c4-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="629c4-109">Létrehoz egy MyAccount nevű új Azure Maps-fiókot az erőforrás csoport MyResourceGroup az SKU S0 és egy címkével.</span><span class="sxs-lookup"><span data-stu-id="629c4-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="629c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="629c4-110">PARAMETERS</span></span>

### <span data-ttu-id="629c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629c4-111">-DefaultProfile</span></span>
<span data-ttu-id="629c4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="629c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="629c4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="629c4-113">-Force</span></span>
<span data-ttu-id="629c4-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="629c4-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="629c4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="629c4-115">-Name</span></span>
<span data-ttu-id="629c4-116">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="629c4-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="629c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="629c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="629c4-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="629c4-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="629c4-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="629c4-119">-SkuName</span></span>
<span data-ttu-id="629c4-120">A fiók SKU-nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="629c4-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="629c4-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="629c4-121">-Tag</span></span>
<span data-ttu-id="629c4-122">Térképek: a fiókok címkéi.</span><span class="sxs-lookup"><span data-stu-id="629c4-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="629c4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="629c4-123">-Confirm</span></span>
<span data-ttu-id="629c4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="629c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="629c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="629c4-125">-WhatIf</span></span>
<span data-ttu-id="629c4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="629c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="629c4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="629c4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="629c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629c4-128">CommonParameters</span></span>
<span data-ttu-id="629c4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="629c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629c4-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="629c4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629c4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="629c4-131">INPUTS</span></span>

### <span data-ttu-id="629c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="629c4-132">System.String</span></span>

## <span data-ttu-id="629c4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="629c4-133">OUTPUTS</span></span>

### <span data-ttu-id="629c4-134">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="629c4-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="629c4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="629c4-135">NOTES</span></span>

## <span data-ttu-id="629c4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="629c4-136">RELATED LINKS</span></span>
