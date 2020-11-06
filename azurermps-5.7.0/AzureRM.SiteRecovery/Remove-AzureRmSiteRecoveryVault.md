---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 70d0876be32b80d314dfb7a464d0626b7c534fea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492173"
---
# <span data-ttu-id="9c790-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9c790-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="9c790-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c790-102">SYNOPSIS</span></span>
<span data-ttu-id="9c790-103">Eltávolít egy webhely-helyreállítási boltozatot.</span><span class="sxs-lookup"><span data-stu-id="9c790-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c790-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c790-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c790-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c790-105">DESCRIPTION</span></span>
<span data-ttu-id="9c790-106">A **Remove-AzureRmSiteRecoveryVault** parancsmag törli az Azure webhely-helyreállítási boltozatot.</span><span class="sxs-lookup"><span data-stu-id="9c790-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9c790-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c790-107">EXAMPLES</span></span>

## <span data-ttu-id="9c790-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c790-108">PARAMETERS</span></span>

### <span data-ttu-id="9c790-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c790-109">-DefaultProfile</span></span>
<span data-ttu-id="9c790-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c790-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c790-111">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="9c790-111">-Vault</span></span>
<span data-ttu-id="9c790-112">A webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c790-112">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c790-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c790-113">CommonParameters</span></span>
<span data-ttu-id="9c790-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c790-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c790-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c790-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c790-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c790-116">INPUTS</span></span>

### <span data-ttu-id="9c790-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="9c790-117">ASRVault</span></span>
<span data-ttu-id="9c790-118">A "Vault" paraméter az "ASRVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9c790-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="9c790-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c790-119">OUTPUTS</span></span>

## <span data-ttu-id="9c790-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c790-120">NOTES</span></span>

## <span data-ttu-id="9c790-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c790-121">RELATED LINKS</span></span>

[<span data-ttu-id="9c790-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9c790-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="9c790-123">Új – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="9c790-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
