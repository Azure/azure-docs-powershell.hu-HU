---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 66731d988eb0232e4223343349bec05e5a12d44b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665917"
---
# <span data-ttu-id="3e8bd-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="3e8bd-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="3e8bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8bd-103">Azure Maps-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="3e8bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e8bd-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="3e8bd-106">Az New-AzMapsAccount parancsmag létrehoz egy Azure Maps-fiókot a megadott SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="3e8bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e8bd-107">EXAMPLES</span></span>

### <span data-ttu-id="3e8bd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3e8bd-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="3e8bd-109">Létrehoz egy MyAccount nevű új Azure Maps-fiókot az erőforrás csoport MyResourceGroup az SKU S0 és egy címkével.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="3e8bd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e8bd-110">PARAMETERS</span></span>

### <span data-ttu-id="3e8bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8bd-111">-DefaultProfile</span></span>
<span data-ttu-id="3e8bd-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e8bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e8bd-113">-Force</span></span>
<span data-ttu-id="3e8bd-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3e8bd-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e8bd-115">-Name</span></span>
<span data-ttu-id="3e8bd-116">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="3e8bd-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="3e8bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e8bd-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e8bd-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3e8bd-119">-SkuName</span></span>
<span data-ttu-id="3e8bd-120">A fiók SKU-nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="3e8bd-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="3e8bd-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="3e8bd-121">-Tag</span></span>
<span data-ttu-id="3e8bd-122">Térképek: a fiókok címkéi.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="3e8bd-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e8bd-123">-Confirm</span></span>
<span data-ttu-id="3e8bd-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8bd-125">-WhatIf</span></span>
<span data-ttu-id="3e8bd-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e8bd-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e8bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8bd-128">CommonParameters</span></span>
<span data-ttu-id="3e8bd-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e8bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8bd-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8bd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8bd-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e8bd-131">INPUTS</span></span>

### <span data-ttu-id="3e8bd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3e8bd-132">System.String</span></span>

## <span data-ttu-id="3e8bd-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e8bd-133">OUTPUTS</span></span>

### <span data-ttu-id="3e8bd-134">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="3e8bd-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="3e8bd-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e8bd-135">NOTES</span></span>

## <span data-ttu-id="3e8bd-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e8bd-136">RELATED LINKS</span></span>
