---
external help file: Azs.KeyVault.Admin-help.xml
Module Name: Azs.Keyvault.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 435db6fd34e36e6c65b9086b7ac1935f60d86c06
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840753"
---
# <span data-ttu-id="b3d34-101">Get-AzsKeyVaultQuota</span><span class="sxs-lookup"><span data-stu-id="b3d34-101">Get-AzsKeyVaultQuota</span></span>

## <span data-ttu-id="b3d34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3d34-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d34-103">A "minden" lemezkvóta-objektum listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="b3d34-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="b3d34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3d34-104">SYNTAX</span></span>

```
Get-AzsKeyVaultQuota [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b3d34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3d34-105">DESCRIPTION</span></span>
<span data-ttu-id="b3d34-106">A "minden" lemezkvóta-objektum listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="b3d34-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="b3d34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b3d34-107">EXAMPLES</span></span>

### <span data-ttu-id="b3d34-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b3d34-108">EXAMPLE 1</span></span>
```
Get-AzsKeyVaultQuota
```

<span data-ttu-id="b3d34-109">A "minden" lemezkvóta-objektum listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="b3d34-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="b3d34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3d34-110">PARAMETERS</span></span>

### <span data-ttu-id="b3d34-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="b3d34-111">-Location</span></span>
<span data-ttu-id="b3d34-112">A kvóta helye.</span><span class="sxs-lookup"><span data-stu-id="b3d34-112">The location of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d34-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d34-113">CommonParameters</span></span>
<span data-ttu-id="b3d34-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3d34-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d34-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d34-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d34-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3d34-116">INPUTS</span></span>

## <span data-ttu-id="b3d34-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3d34-117">OUTPUTS</span></span>

### <span data-ttu-id="b3d34-118">Microsoft. AzureStack. Management. kulcskezelő. admin. models. kvóta</span><span class="sxs-lookup"><span data-stu-id="b3d34-118">Microsoft.AzureStack.Management.KeyVault.Admin.Models.Quota</span></span>

## <span data-ttu-id="b3d34-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3d34-119">NOTES</span></span>

## <span data-ttu-id="b3d34-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3d34-120">RELATED LINKS</span></span>
