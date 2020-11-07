---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 80887622c5a9dbc3c6ddf544d435974b8212d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672764"
---
# <span data-ttu-id="2db82-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2db82-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="2db82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2db82-102">SYNOPSIS</span></span>
<span data-ttu-id="2db82-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="2db82-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2db82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2db82-104">SYNTAX</span></span>

### <span data-ttu-id="2db82-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="2db82-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db82-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="2db82-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db82-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2db82-107">DESCRIPTION</span></span>
<span data-ttu-id="2db82-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="2db82-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2db82-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2db82-109">EXAMPLES</span></span>

### <span data-ttu-id="2db82-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2db82-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2db82-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="2db82-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="2db82-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2db82-112">PARAMETERS</span></span>

### <span data-ttu-id="2db82-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2db82-113">-ExpandResource</span></span>
<span data-ttu-id="2db82-114">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="2db82-114">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db82-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2db82-115">-Name</span></span>
<span data-ttu-id="2db82-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2db82-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db82-117">-ResourceGroupName</span></span>
<span data-ttu-id="2db82-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2db82-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db82-119">-DefaultProfile</span></span>
<span data-ttu-id="2db82-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2db82-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2db82-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db82-121">CommonParameters</span></span>
<span data-ttu-id="2db82-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2db82-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db82-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db82-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db82-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db82-124">INPUTS</span></span>

### <span data-ttu-id="2db82-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2db82-125">System.String</span></span>

## <span data-ttu-id="2db82-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db82-126">OUTPUTS</span></span>

### <span data-ttu-id="2db82-127">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2db82-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2db82-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2db82-128">NOTES</span></span>

## <span data-ttu-id="2db82-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2db82-129">RELATED LINKS</span></span>

