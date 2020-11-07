---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680478"
---
# <span data-ttu-id="b11cb-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b11cb-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="b11cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b11cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b11cb-103">Eltávolítja a webhely-helyreállítási kiszolgálót az aktuális boltozatról.</span><span class="sxs-lookup"><span data-stu-id="b11cb-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b11cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b11cb-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b11cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b11cb-105">DESCRIPTION</span></span>
<span data-ttu-id="b11cb-106">A **Remove-AzureRmSiteRecoveryServer** parancsmag megszünteti az Azure-webhely helyreállítási kiszolgálóját, amely eltávolítja azt az aktuális boltozatról.</span><span class="sxs-lookup"><span data-stu-id="b11cb-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="b11cb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b11cb-107">EXAMPLES</span></span>

## <span data-ttu-id="b11cb-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b11cb-108">PARAMETERS</span></span>

### <span data-ttu-id="b11cb-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b11cb-109">-Force</span></span>
<span data-ttu-id="b11cb-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b11cb-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11cb-111">-Server</span><span class="sxs-lookup"><span data-stu-id="b11cb-111">-Server</span></span>
<span data-ttu-id="b11cb-112">A webhely-helyreállítási kiszolgáló objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b11cb-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b11cb-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b11cb-113">-Confirm</span></span>
<span data-ttu-id="b11cb-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b11cb-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11cb-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b11cb-115">-WhatIf</span></span>
<span data-ttu-id="b11cb-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b11cb-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b11cb-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b11cb-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11cb-118">-DefaultProfile</span></span>
<span data-ttu-id="b11cb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b11cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11cb-120">CommonParameters</span></span>
<span data-ttu-id="b11cb-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b11cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11cb-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11cb-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b11cb-123">INPUTS</span></span>

### <span data-ttu-id="b11cb-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="b11cb-124">ASRServer</span></span>
<span data-ttu-id="b11cb-125">A ' kiszolgáló ' paraméter elfogadja a "ASRServer" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b11cb-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="b11cb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b11cb-126">OUTPUTS</span></span>

### <span data-ttu-id="b11cb-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="b11cb-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="b11cb-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b11cb-128">NOTES</span></span>

## <span data-ttu-id="b11cb-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b11cb-129">RELATED LINKS</span></span>

[<span data-ttu-id="b11cb-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b11cb-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="b11cb-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b11cb-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
