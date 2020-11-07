---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679689"
---
# <span data-ttu-id="dffbd-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="dffbd-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="dffbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dffbd-102">SYNOPSIS</span></span>
<span data-ttu-id="dffbd-103">Információt kap az aktuális boltozathoz regisztrált webhely-helyreállítási kiszolgálókról.</span><span class="sxs-lookup"><span data-stu-id="dffbd-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dffbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dffbd-104">SYNTAX</span></span>

### <span data-ttu-id="dffbd-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dffbd-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffbd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dffbd-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffbd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dffbd-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dffbd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dffbd-108">DESCRIPTION</span></span>
<span data-ttu-id="dffbd-109">A **Get-AzureRmSiteRecoveryServer** parancsmag a jelenlegi webhely-helyreállítási boltozathoz regisztrált Azure-webhelyek helyreállítási kiszolgálóiról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="dffbd-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="dffbd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dffbd-110">EXAMPLES</span></span>

## <span data-ttu-id="dffbd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dffbd-111">PARAMETERS</span></span>

### <span data-ttu-id="dffbd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffbd-112">-DefaultProfile</span></span>
<span data-ttu-id="dffbd-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dffbd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dffbd-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="dffbd-114">-FriendlyName</span></span>
<span data-ttu-id="dffbd-115">A kiszolgáló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dffbd-115">Specifies the friendly name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffbd-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dffbd-116">-Name</span></span>
<span data-ttu-id="dffbd-117">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dffbd-117">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffbd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffbd-118">CommonParameters</span></span>
<span data-ttu-id="dffbd-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dffbd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffbd-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dffbd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffbd-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dffbd-121">INPUTS</span></span>

### <span data-ttu-id="dffbd-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="dffbd-122">None</span></span>
<span data-ttu-id="dffbd-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dffbd-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dffbd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dffbd-124">OUTPUTS</span></span>

### <span data-ttu-id="dffbd-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="dffbd-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="dffbd-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dffbd-126">NOTES</span></span>

## <span data-ttu-id="dffbd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dffbd-127">RELATED LINKS</span></span>

[<span data-ttu-id="dffbd-128">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="dffbd-128">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
