---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679682"
---
# <span data-ttu-id="38570-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="38570-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="38570-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38570-102">SYNOPSIS</span></span>
<span data-ttu-id="38570-103">Webhely-helyreállítási boltozatokat kap a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="38570-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38570-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38570-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38570-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38570-105">DESCRIPTION</span></span>
<span data-ttu-id="38570-106">A **Get-AzureRmSiteRecoveryVault** parancsmag a jelenlegi előfizetésből kapja meg az Azure webhelyek helyreállítási boltozatai vagy egy bizonyos webhely-helyreállítási tároló listáját.</span><span class="sxs-lookup"><span data-stu-id="38570-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="38570-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38570-107">EXAMPLES</span></span>

## <span data-ttu-id="38570-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38570-108">PARAMETERS</span></span>

### <span data-ttu-id="38570-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38570-109">-DefaultProfile</span></span>
<span data-ttu-id="38570-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38570-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38570-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38570-111">-Name</span></span>
<span data-ttu-id="38570-112">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38570-112">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38570-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38570-113">-ResourceGroupName</span></span>
<span data-ttu-id="38570-114">Annak az Azure erőforrás-csoportnak a nevét adja meg, amelyből a helyreállítási szolgáltatások objektumot be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="38570-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38570-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38570-115">CommonParameters</span></span>
<span data-ttu-id="38570-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38570-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38570-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38570-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38570-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38570-118">INPUTS</span></span>

### <span data-ttu-id="38570-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="38570-119">None</span></span>
<span data-ttu-id="38570-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="38570-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38570-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38570-121">OUTPUTS</span></span>

### <span data-ttu-id="38570-122">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="38570-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="38570-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38570-123">NOTES</span></span>

## <span data-ttu-id="38570-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38570-124">RELATED LINKS</span></span>

[<span data-ttu-id="38570-125">Új – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="38570-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="38570-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="38570-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
