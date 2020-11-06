---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 60e380ffd046c61abb218395a838c6e0d5d785f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493454"
---
# <span data-ttu-id="ac93c-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="ac93c-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="ac93c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac93c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac93c-103">Az összes elérhető SSL-beállítás beolvasása az alkalmazás-átjáró SSL-házirendjében.</span><span class="sxs-lookup"><span data-stu-id="ac93c-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac93c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac93c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac93c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac93c-105">DESCRIPTION</span></span>
<span data-ttu-id="ac93c-106">A **Get-AzureRmApplicationGatewayAvailableSslOptions** parancsmag az SSL-házirend minden elérhető SSL-beállítását megkapja</span><span class="sxs-lookup"><span data-stu-id="ac93c-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="ac93c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ac93c-107">EXAMPLES</span></span>

### <span data-ttu-id="ac93c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac93c-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="ac93c-109">Ez a parancs az SSL-házirend minden elérhető SSL-beállítását visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="ac93c-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="ac93c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac93c-110">PARAMETERS</span></span>

### <span data-ttu-id="ac93c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac93c-111">-DefaultProfile</span></span>
<span data-ttu-id="ac93c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac93c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac93c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac93c-113">CommonParameters</span></span>
<span data-ttu-id="ac93c-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac93c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac93c-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac93c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac93c-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac93c-116">INPUTS</span></span>

### <span data-ttu-id="ac93c-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac93c-117">None</span></span>

## <span data-ttu-id="ac93c-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac93c-118">OUTPUTS</span></span>

### <span data-ttu-id="ac93c-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="ac93c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="ac93c-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac93c-120">NOTES</span></span>

## <span data-ttu-id="ac93c-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac93c-121">RELATED LINKS</span></span>

