---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: d54314686edafba9e72872411c678905adc55f47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680527"
---
# <span data-ttu-id="1ae15-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1ae15-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="1ae15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ae15-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae15-103">Információkat kap a médiával kapcsolatos szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="1ae15-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae15-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ae15-104">SYNTAX</span></span>

### <span data-ttu-id="1ae15-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae15-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae15-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae15-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae15-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ae15-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae15-108">A **Get-AzureRmMediaService** parancsmag információkat kap a multimédiás szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="1ae15-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="1ae15-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1ae15-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae15-110">Példa 1: az erőforráscsoport összes médiafájljának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1ae15-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="1ae15-111">Ez a parancs a ResourceGroup001 nevű erőforráscsoport minden médiafájljának tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="1ae15-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="1ae15-112">2. példa: a médiaadatfolyam-szolgáltatás tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="1ae15-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="1ae15-113">Ez a parancs beolvassa a MediaService1 nevű Media Service tulajdonságát, amely a ResourceGroup002 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="1ae15-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="1ae15-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ae15-114">PARAMETERS</span></span>

### <span data-ttu-id="1ae15-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ae15-115">-AccountName</span></span>
<span data-ttu-id="1ae15-116">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="1ae15-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae15-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae15-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ae15-118">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ae15-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1ae15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae15-119">-DefaultProfile</span></span>
<span data-ttu-id="1ae15-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ae15-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae15-121">CommonParameters</span></span>
<span data-ttu-id="1ae15-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ae15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae15-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae15-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae15-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae15-124">INPUTS</span></span>

## <span data-ttu-id="1ae15-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae15-125">OUTPUTS</span></span>

### <span data-ttu-id="1ae15-126">Microsoft. Azure. commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="1ae15-126">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="1ae15-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ae15-127">NOTES</span></span>

## <span data-ttu-id="1ae15-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ae15-128">RELATED LINKS</span></span>

[<span data-ttu-id="1ae15-129">Új – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1ae15-129">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="1ae15-130">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1ae15-130">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="1ae15-131">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="1ae15-131">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


