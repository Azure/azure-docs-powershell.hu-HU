---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493000"
---
# <span data-ttu-id="52f40-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="52f40-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="52f40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52f40-102">SYNOPSIS</span></span>
<span data-ttu-id="52f40-103">A webhely-helyreállítási védelem házirendjeit kapja.</span><span class="sxs-lookup"><span data-stu-id="52f40-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52f40-104">SYNTAX</span></span>

### <span data-ttu-id="52f40-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52f40-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52f40-106">ByName</span><span class="sxs-lookup"><span data-stu-id="52f40-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52f40-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="52f40-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52f40-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="52f40-108">DESCRIPTION</span></span>
<span data-ttu-id="52f40-109">A **Get-AzureRmSiteRecoveryPolicy** parancsmag a beállított Azure-webhely-helyreállítási védelmi házirendek listáját, illetve egy bizonyos védelmi házirendet tartalmaz a név szerint.</span><span class="sxs-lookup"><span data-stu-id="52f40-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="52f40-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52f40-110">EXAMPLES</span></span>

## <span data-ttu-id="52f40-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52f40-111">PARAMETERS</span></span>

### <span data-ttu-id="52f40-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f40-112">-DefaultProfile</span></span>
<span data-ttu-id="52f40-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52f40-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f40-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="52f40-114">-FriendlyName</span></span>
<span data-ttu-id="52f40-115">A webhely-helyreállítási replikációs házirend rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52f40-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="52f40-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52f40-116">-Name</span></span>
<span data-ttu-id="52f40-117">A webhely-helyreállítási replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52f40-117">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="52f40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f40-118">CommonParameters</span></span>
<span data-ttu-id="52f40-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52f40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f40-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f40-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f40-121">INPUTS</span></span>

### <span data-ttu-id="52f40-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="52f40-122">None</span></span>
<span data-ttu-id="52f40-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="52f40-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52f40-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f40-124">OUTPUTS</span></span>

### <span data-ttu-id="52f40-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="52f40-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="52f40-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52f40-126">NOTES</span></span>

## <span data-ttu-id="52f40-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52f40-127">RELATED LINKS</span></span>

[<span data-ttu-id="52f40-128">Új – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="52f40-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="52f40-129">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="52f40-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
