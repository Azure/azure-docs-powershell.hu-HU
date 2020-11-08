---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194597"
---
# <span data-ttu-id="2d3d5-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="2d3d5-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="2d3d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3d5-103">A Media szolgáltatáshoz társított REST-végpont eléréséhez szükséges legfontosabb információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d3d5-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="2d3d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d3d5-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d3d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d3d5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d3d5-106">A **Get-AzMediaServiceKey** parancsmag fontos információkat kap az Azure Media szolgáltatáshoz társított reprezentációs State Transfer (REST) végpont eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="2d3d5-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="2d3d5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d3d5-107">EXAMPLES</span></span>

### <span data-ttu-id="2d3d5-108">1. példa: a fontos információk beszerzése a Media szolgáltatás eléréséhez</span><span class="sxs-lookup"><span data-stu-id="2d3d5-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="2d3d5-109">Ez a parancs a MediaService001 nevű Media szolgáltatás eléréséhez szükséges főbb információkat kapja, amelyek a ResourceGroup001 nevű erőforráscsoport csoportjába tartoznak.</span><span class="sxs-lookup"><span data-stu-id="2d3d5-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="2d3d5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d3d5-110">PARAMETERS</span></span>

### <span data-ttu-id="2d3d5-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d3d5-111">-AccountName</span></span>
<span data-ttu-id="2d3d5-112">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag a médiaszolgáltató kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="2d3d5-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3d5-113">-DefaultProfile</span></span>
<span data-ttu-id="2d3d5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d3d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d3d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d3d5-116">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d3d5-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="2d3d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3d5-117">CommonParameters</span></span>
<span data-ttu-id="2d3d5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d3d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3d5-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3d5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3d5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d3d5-120">INPUTS</span></span>

### <span data-ttu-id="2d3d5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2d3d5-121">System.String</span></span>

## <span data-ttu-id="2d3d5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d3d5-122">OUTPUTS</span></span>

### <span data-ttu-id="2d3d5-123">Microsoft. Azure. commands. Media. models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="2d3d5-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="2d3d5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d3d5-124">NOTES</span></span>

## <span data-ttu-id="2d3d5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d3d5-125">RELATED LINKS</span></span>

[<span data-ttu-id="2d3d5-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="2d3d5-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


