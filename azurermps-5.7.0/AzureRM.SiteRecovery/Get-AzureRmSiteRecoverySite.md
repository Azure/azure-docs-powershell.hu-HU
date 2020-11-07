---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679686"
---
# <span data-ttu-id="3a806-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="3a806-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="3a806-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a806-102">SYNOPSIS</span></span>
<span data-ttu-id="3a806-103">A Hyper-V-webhelyeket a webhely-helyreállítási boltozatból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a806-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a806-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a806-104">SYNTAX</span></span>

### <span data-ttu-id="3a806-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a806-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a806-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3a806-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a806-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3a806-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a806-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a806-108">DESCRIPTION</span></span>
<span data-ttu-id="3a806-109">A **Get-AzureRmSiteRecoverySite** parancsmag a Hyper-V-webhelyeket az Azure-webhely helyreállítási pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="3a806-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="3a806-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3a806-110">EXAMPLES</span></span>

## <span data-ttu-id="3a806-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a806-111">PARAMETERS</span></span>

### <span data-ttu-id="3a806-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a806-112">-DefaultProfile</span></span>
<span data-ttu-id="3a806-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a806-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a806-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="3a806-114">-FriendlyName</span></span>
<span data-ttu-id="3a806-115">A webhely rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a806-115">Specifies the friendly name of the site.</span></span>

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

### <span data-ttu-id="3a806-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a806-116">-Name</span></span>
<span data-ttu-id="3a806-117">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a806-117">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="3a806-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a806-118">CommonParameters</span></span>
<span data-ttu-id="3a806-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a806-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a806-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a806-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a806-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a806-121">INPUTS</span></span>

### <span data-ttu-id="3a806-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a806-122">None</span></span>
<span data-ttu-id="3a806-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3a806-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a806-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a806-124">OUTPUTS</span></span>

### <span data-ttu-id="3a806-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="3a806-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="3a806-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a806-126">NOTES</span></span>

## <span data-ttu-id="3a806-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a806-127">RELATED LINKS</span></span>

[<span data-ttu-id="3a806-128">Új – AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="3a806-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="3a806-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="3a806-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
