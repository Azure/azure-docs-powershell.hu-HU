---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195796"
---
# <span data-ttu-id="f4906-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f4906-101">Get-AzMediaService</span></span>

## <span data-ttu-id="f4906-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4906-102">SYNOPSIS</span></span>
<span data-ttu-id="f4906-103">Információkat kap a médiával kapcsolatos szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="f4906-103">Gets information about a media service.</span></span>

## <span data-ttu-id="f4906-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4906-104">SYNTAX</span></span>

### <span data-ttu-id="f4906-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4906-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4906-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4906-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4906-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4906-107">DESCRIPTION</span></span>
<span data-ttu-id="f4906-108">A **Get-AzMediaService** parancsmag információkat kap a multimédiás szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="f4906-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="f4906-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f4906-109">EXAMPLES</span></span>

### <span data-ttu-id="f4906-110">Példa 1: az erőforráscsoport összes médiafájljának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f4906-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="f4906-111">Ez a parancs a ResourceGroup001 nevű erőforráscsoport minden médiafájljának tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="f4906-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f4906-112">2. példa: a médiaadatfolyam-szolgáltatás tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f4906-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="f4906-113">Ez a parancs beolvassa a MediaService1 nevű Media Service tulajdonságát, amely a ResourceGroup002 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="f4906-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f4906-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4906-114">PARAMETERS</span></span>

### <span data-ttu-id="f4906-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4906-115">-AccountName</span></span>
<span data-ttu-id="f4906-116">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="f4906-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4906-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4906-117">-DefaultProfile</span></span>
<span data-ttu-id="f4906-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f4906-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4906-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4906-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4906-120">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4906-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f4906-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4906-121">CommonParameters</span></span>
<span data-ttu-id="f4906-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4906-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4906-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4906-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4906-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4906-124">INPUTS</span></span>

### <span data-ttu-id="f4906-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f4906-125">System.String</span></span>

## <span data-ttu-id="f4906-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4906-126">OUTPUTS</span></span>

### <span data-ttu-id="f4906-127">Microsoft. Azure. commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="f4906-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f4906-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4906-128">NOTES</span></span>

## <span data-ttu-id="f4906-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4906-129">RELATED LINKS</span></span>

[<span data-ttu-id="f4906-130">Új – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f4906-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="f4906-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f4906-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f4906-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f4906-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


