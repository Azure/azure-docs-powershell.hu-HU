---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679930"
---
# <span data-ttu-id="f8edc-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="f8edc-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="f8edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8edc-102">SYNOPSIS</span></span>
<span data-ttu-id="f8edc-103">Információt kap az aktuális boltozathoz regisztrált webhely-helyreállítási kiszolgálókról.</span><span class="sxs-lookup"><span data-stu-id="f8edc-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8edc-104">SYNTAX</span></span>

### <span data-ttu-id="f8edc-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8edc-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8edc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f8edc-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8edc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f8edc-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8edc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8edc-108">DESCRIPTION</span></span>
<span data-ttu-id="f8edc-109">A **Get-AzureRmSiteRecoveryServer** parancsmag a jelenlegi webhely-helyreállítási boltozathoz regisztrált Azure-webhelyek helyreállítási kiszolgálóiról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="f8edc-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="f8edc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f8edc-110">EXAMPLES</span></span>

## <span data-ttu-id="f8edc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8edc-111">PARAMETERS</span></span>

### <span data-ttu-id="f8edc-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="f8edc-112">-FriendlyName</span></span>
<span data-ttu-id="f8edc-113">A kiszolgáló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8edc-113">Specifies the friendly name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8edc-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8edc-114">-Name</span></span>
<span data-ttu-id="f8edc-115">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8edc-115">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8edc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8edc-116">-DefaultProfile</span></span>
<span data-ttu-id="f8edc-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8edc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8edc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8edc-118">CommonParameters</span></span>
<span data-ttu-id="f8edc-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8edc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8edc-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8edc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8edc-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8edc-121">INPUTS</span></span>

## <span data-ttu-id="f8edc-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8edc-122">OUTPUTS</span></span>

### <span data-ttu-id="f8edc-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="f8edc-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="f8edc-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8edc-124">NOTES</span></span>

## <span data-ttu-id="f8edc-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8edc-125">RELATED LINKS</span></span>

[<span data-ttu-id="f8edc-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="f8edc-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
