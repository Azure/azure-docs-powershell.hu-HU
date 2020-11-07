---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableSslOption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: e0fa27a99a8a2d00819d558b42218b9405a5f039
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841765"
---
# <span data-ttu-id="f999e-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="f999e-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="f999e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f999e-102">SYNOPSIS</span></span>
<span data-ttu-id="f999e-103">Az összes elérhető SSL-beállítás beolvasása az alkalmazás-átjáró SSL-házirendjében.</span><span class="sxs-lookup"><span data-stu-id="f999e-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="f999e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f999e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f999e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f999e-105">DESCRIPTION</span></span>
<span data-ttu-id="f999e-106">A **Get-AzApplicationGatewayAvailableSslOption** parancsmag az SSL-házirend minden elérhető SSL-beállítását megkapja</span><span class="sxs-lookup"><span data-stu-id="f999e-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="f999e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f999e-107">EXAMPLES</span></span>

### <span data-ttu-id="f999e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f999e-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="f999e-109">Ez a parancs az SSL-házirend minden elérhető SSL-beállítását visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="f999e-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="f999e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f999e-110">PARAMETERS</span></span>

### <span data-ttu-id="f999e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f999e-111">-DefaultProfile</span></span>
<span data-ttu-id="f999e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f999e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f999e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f999e-113">CommonParameters</span></span>
<span data-ttu-id="f999e-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f999e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f999e-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f999e-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f999e-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f999e-116">INPUTS</span></span>

### <span data-ttu-id="f999e-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="f999e-117">None</span></span>

## <span data-ttu-id="f999e-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f999e-118">OUTPUTS</span></span>

### <span data-ttu-id="f999e-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="f999e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="f999e-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f999e-120">NOTES</span></span>

## <span data-ttu-id="f999e-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f999e-121">RELATED LINKS</span></span>

