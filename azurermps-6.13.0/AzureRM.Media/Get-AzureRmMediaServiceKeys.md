---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 7aab48c69dc1e10d35c49de2d1dff427d5df2c41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679545"
---
# <span data-ttu-id="0f3fa-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="0f3fa-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="0f3fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3fa-103">A Media szolgáltatáshoz társított REST-végpont eléréséhez szükséges legfontosabb információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0f3fa-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f3fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f3fa-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f3fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f3fa-105">DESCRIPTION</span></span>
<span data-ttu-id="0f3fa-106">A **Get-AzureRmMediaServiceKeys** parancsmag fontos információkat kap az Azure Media szolgáltatáshoz társított reprezentációs State Transfer (REST) végpont eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="0f3fa-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="0f3fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f3fa-107">EXAMPLES</span></span>

### <span data-ttu-id="0f3fa-108">1. példa: a fontos információk beszerzése a Media szolgáltatás eléréséhez</span><span class="sxs-lookup"><span data-stu-id="0f3fa-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="0f3fa-109">Ez a parancs a MediaService001 nevű Media szolgáltatás eléréséhez szükséges főbb információkat kapja, amelyek a ResourceGroup001 nevű erőforráscsoport csoportjába tartoznak.</span><span class="sxs-lookup"><span data-stu-id="0f3fa-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="0f3fa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f3fa-110">PARAMETERS</span></span>

### <span data-ttu-id="0f3fa-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f3fa-111">-AccountName</span></span>
<span data-ttu-id="0f3fa-112">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag a médiaszolgáltató kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="0f3fa-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="0f3fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3fa-113">-DefaultProfile</span></span>
<span data-ttu-id="0f3fa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f3fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f3fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f3fa-116">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f3fa-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="0f3fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3fa-117">CommonParameters</span></span>
<span data-ttu-id="0f3fa-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f3fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3fa-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f3fa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3fa-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f3fa-120">INPUTS</span></span>

### <span data-ttu-id="0f3fa-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0f3fa-121">System.String</span></span>

## <span data-ttu-id="0f3fa-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f3fa-122">OUTPUTS</span></span>

### <span data-ttu-id="0f3fa-123">Microsoft. Azure. commands. Media. models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="0f3fa-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="0f3fa-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f3fa-124">NOTES</span></span>

## <span data-ttu-id="0f3fa-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f3fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="0f3fa-126">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="0f3fa-126">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


