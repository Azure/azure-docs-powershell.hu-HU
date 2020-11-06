---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: a83b4b8ca3dbe415013fe9a858d46cb886ce4b00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492175"
---
# <span data-ttu-id="09fa9-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="09fa9-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="09fa9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="09fa9-103">Eltávolítja a webhely-helyreállítási webhelyet az aktuális boltozatról.</span><span class="sxs-lookup"><span data-stu-id="09fa9-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09fa9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09fa9-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fa9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="09fa9-106">A **Remove-AzureRmSiteRecoverySite** parancsmag egy Azure webhely-helyreállítási webhelyet töröl az aktuális boltozatról.</span><span class="sxs-lookup"><span data-stu-id="09fa9-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="09fa9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09fa9-107">EXAMPLES</span></span>

## <span data-ttu-id="09fa9-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09fa9-108">PARAMETERS</span></span>

### <span data-ttu-id="09fa9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fa9-109">-DefaultProfile</span></span>
<span data-ttu-id="09fa9-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09fa9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09fa9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="09fa9-111">-Force</span></span>
<span data-ttu-id="09fa9-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="09fa9-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fa9-113">-Webhely</span><span class="sxs-lookup"><span data-stu-id="09fa9-113">-Site</span></span>
<span data-ttu-id="09fa9-114">A webhely-helyreállítási webhely objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09fa9-114">Specifies the Site Recovery site object.</span></span>

```yaml
Type: ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09fa9-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09fa9-115">-Confirm</span></span>
<span data-ttu-id="09fa9-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09fa9-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fa9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fa9-117">-WhatIf</span></span>
<span data-ttu-id="09fa9-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09fa9-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="09fa9-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09fa9-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fa9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fa9-120">CommonParameters</span></span>
<span data-ttu-id="09fa9-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09fa9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fa9-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fa9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fa9-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09fa9-123">INPUTS</span></span>

### <span data-ttu-id="09fa9-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="09fa9-124">ASRSite</span></span>
<span data-ttu-id="09fa9-125">A "webhely" paraméter elfogadja a "ASRSite" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="09fa9-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="09fa9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09fa9-126">OUTPUTS</span></span>

## <span data-ttu-id="09fa9-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09fa9-127">NOTES</span></span>

## <span data-ttu-id="09fa9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09fa9-128">RELATED LINKS</span></span>

[<span data-ttu-id="09fa9-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="09fa9-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="09fa9-130">Új – AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="09fa9-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
