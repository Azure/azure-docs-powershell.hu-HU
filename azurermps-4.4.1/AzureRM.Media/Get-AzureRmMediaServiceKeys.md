---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680525"
---
# <span data-ttu-id="f87cd-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f87cd-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="f87cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f87cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f87cd-103">A Media szolgáltatáshoz társított REST-végpont eléréséhez szükséges legfontosabb információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f87cd-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f87cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f87cd-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f87cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f87cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f87cd-106">A **Get-AzureRmMediaServiceKeys** parancsmag fontos információkat kap az Azure Media szolgáltatáshoz társított reprezentációs State Transfer (REST) végpont eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f87cd-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="f87cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f87cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f87cd-108">1. példa: a fontos információk beszerzése a Media szolgáltatás eléréséhez</span><span class="sxs-lookup"><span data-stu-id="f87cd-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="f87cd-109">Ez a parancs a MediaService001 nevű Media szolgáltatás eléréséhez szükséges főbb információkat kapja, amelyek a ResourceGroup001 nevű erőforráscsoport csoportjába tartoznak.</span><span class="sxs-lookup"><span data-stu-id="f87cd-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="f87cd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f87cd-110">PARAMETERS</span></span>

### <span data-ttu-id="f87cd-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f87cd-111">-AccountName</span></span>
<span data-ttu-id="f87cd-112">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag a médiaszolgáltató kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="f87cd-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="f87cd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87cd-113">-ResourceGroupName</span></span>
<span data-ttu-id="f87cd-114">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f87cd-114">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f87cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87cd-115">-DefaultProfile</span></span>
<span data-ttu-id="f87cd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f87cd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f87cd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87cd-117">CommonParameters</span></span>
<span data-ttu-id="f87cd-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f87cd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87cd-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87cd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87cd-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f87cd-120">INPUTS</span></span>

## <span data-ttu-id="f87cd-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f87cd-121">OUTPUTS</span></span>

### <span data-ttu-id="f87cd-122">Microsoft. Azure. commands. Media. models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f87cd-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="f87cd-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f87cd-123">NOTES</span></span>

## <span data-ttu-id="f87cd-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f87cd-124">RELATED LINKS</span></span>

[<span data-ttu-id="f87cd-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f87cd-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


