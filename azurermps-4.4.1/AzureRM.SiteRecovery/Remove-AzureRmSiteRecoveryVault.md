---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500688"
---
# <span data-ttu-id="a28cb-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a28cb-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="a28cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a28cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a28cb-103">Eltávolít egy webhely-helyreállítási boltozatot.</span><span class="sxs-lookup"><span data-stu-id="a28cb-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a28cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a28cb-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a28cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a28cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a28cb-106">A **Remove-AzureRmSiteRecoveryVault** parancsmag törli az Azure webhely-helyreállítási boltozatot.</span><span class="sxs-lookup"><span data-stu-id="a28cb-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a28cb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a28cb-107">EXAMPLES</span></span>

## <span data-ttu-id="a28cb-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a28cb-108">PARAMETERS</span></span>

### <span data-ttu-id="a28cb-109">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="a28cb-109">-Vault</span></span>
<span data-ttu-id="a28cb-110">A webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a28cb-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a28cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28cb-111">-DefaultProfile</span></span>
<span data-ttu-id="a28cb-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a28cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a28cb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28cb-113">CommonParameters</span></span>
<span data-ttu-id="a28cb-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a28cb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28cb-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28cb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28cb-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a28cb-116">INPUTS</span></span>

### <span data-ttu-id="a28cb-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="a28cb-117">ASRVault</span></span>
<span data-ttu-id="a28cb-118">A "Vault" paraméter az "ASRVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a28cb-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="a28cb-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a28cb-119">OUTPUTS</span></span>

## <span data-ttu-id="a28cb-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a28cb-120">NOTES</span></span>

## <span data-ttu-id="a28cb-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a28cb-121">RELATED LINKS</span></span>

[<span data-ttu-id="a28cb-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a28cb-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="a28cb-123">Új – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a28cb-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
