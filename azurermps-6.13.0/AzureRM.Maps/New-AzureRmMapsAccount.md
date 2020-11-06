---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
ms.openlocfilehash: 0b8bfad1b3bb9f24c6b7c74e92f64c64d776c2d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497355"
---
# <span data-ttu-id="8405b-101">New-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="8405b-101">New-AzureRmMapsAccount</span></span>

## <span data-ttu-id="8405b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8405b-102">SYNOPSIS</span></span>
<span data-ttu-id="8405b-103">Azure Maps-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8405b-103">Creates an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8405b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8405b-104">SYNTAX</span></span>

```
New-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8405b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8405b-105">DESCRIPTION</span></span>
<span data-ttu-id="8405b-106">Az New-AzureRmMapsAccount parancsmag létrehoz egy Azure Maps-fiókot a megadott SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="8405b-106">The New-AzureRmMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="8405b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8405b-107">EXAMPLES</span></span>

### <span data-ttu-id="8405b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8405b-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="8405b-109">Létrehoz egy MyAccount nevű új Azure Maps-fiókot az erőforrás csoport MyResourceGroup az SKU S0 és egy címkével.</span><span class="sxs-lookup"><span data-stu-id="8405b-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="8405b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8405b-110">PARAMETERS</span></span>

### <span data-ttu-id="8405b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8405b-111">-DefaultProfile</span></span>
<span data-ttu-id="8405b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8405b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8405b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8405b-113">-Force</span></span>
<span data-ttu-id="8405b-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8405b-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8405b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8405b-115">-Name</span></span>
<span data-ttu-id="8405b-116">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="8405b-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="8405b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8405b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8405b-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8405b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="8405b-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8405b-119">-SkuName</span></span>
<span data-ttu-id="8405b-120">A fiók SKU-nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="8405b-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8405b-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="8405b-121">-Tag</span></span>
<span data-ttu-id="8405b-122">Térképek: a fiókok címkéi.</span><span class="sxs-lookup"><span data-stu-id="8405b-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="8405b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8405b-123">-Confirm</span></span>
<span data-ttu-id="8405b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8405b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8405b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8405b-125">-WhatIf</span></span>
<span data-ttu-id="8405b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8405b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8405b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8405b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8405b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8405b-128">CommonParameters</span></span>
<span data-ttu-id="8405b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8405b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8405b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8405b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8405b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8405b-131">INPUTS</span></span>

### <span data-ttu-id="8405b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8405b-132">System.String</span></span>

## <span data-ttu-id="8405b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8405b-133">OUTPUTS</span></span>

### <span data-ttu-id="8405b-134">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="8405b-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="8405b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8405b-135">NOTES</span></span>

## <span data-ttu-id="8405b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8405b-136">RELATED LINKS</span></span>
