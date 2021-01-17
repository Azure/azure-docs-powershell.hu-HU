---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467629"
---
# <span data-ttu-id="b68bc-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b68bc-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="b68bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b68bc-103">Létrehoz egy Azure Maps-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b68bc-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="b68bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b68bc-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b68bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b68bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b68bc-106">A New-AzMapsAccount parancsmag létrehoz egy Azure Maps-fiókot a megadott termékváltozatkal.</span><span class="sxs-lookup"><span data-stu-id="b68bc-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="b68bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b68bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b68bc-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b68bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="b68bc-109">Létrehoz egy MyAccount nevű új Azure Maps-fiókot a MyResourceGroup erőforráscsoportban az SKU S0-val és egy címkével.</span><span class="sxs-lookup"><span data-stu-id="b68bc-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="b68bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b68bc-110">PARAMETERS</span></span>

### <span data-ttu-id="b68bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68bc-111">-DefaultProfile</span></span>
<span data-ttu-id="b68bc-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b68bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b68bc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b68bc-113">-Force</span></span>
<span data-ttu-id="b68bc-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b68bc-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b68bc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b68bc-115">-Name</span></span>
<span data-ttu-id="b68bc-116">Térképek-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b68bc-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="b68bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b68bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="b68bc-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b68bc-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b68bc-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b68bc-119">-SkuName</span></span>
<span data-ttu-id="b68bc-120">Térképek-fiók termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="b68bc-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="b68bc-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="b68bc-121">-Tag</span></span>
<span data-ttu-id="b68bc-122">Térképek fiókcímkék.</span><span class="sxs-lookup"><span data-stu-id="b68bc-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="b68bc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b68bc-123">-Confirm</span></span>
<span data-ttu-id="b68bc-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b68bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b68bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b68bc-125">-WhatIf</span></span>
<span data-ttu-id="b68bc-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b68bc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b68bc-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b68bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b68bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68bc-128">CommonParameters</span></span>
<span data-ttu-id="b68bc-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68bc-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b68bc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68bc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b68bc-131">INPUTS</span></span>

### <span data-ttu-id="b68bc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b68bc-132">System.String</span></span>

## <span data-ttu-id="b68bc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b68bc-133">OUTPUTS</span></span>

### <span data-ttu-id="b68bc-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b68bc-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b68bc-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b68bc-135">NOTES</span></span>

## <span data-ttu-id="b68bc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b68bc-136">RELATED LINKS</span></span>
