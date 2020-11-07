---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 0b70fe2636ae0bc460afd05f9428708c0ff4963b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679673"
---
# <span data-ttu-id="cc645-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="cc645-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="cc645-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc645-102">SYNOPSIS</span></span>
<span data-ttu-id="cc645-103">Webhely-helyreállítási szolgáltatások boltozatának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="cc645-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc645-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc645-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc645-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc645-105">DESCRIPTION</span></span>
<span data-ttu-id="cc645-106">A **New-AzureRmSiteRecoveryVault** parancsmag létrehoz egy Azure site Recovery Services Vault-t.</span><span class="sxs-lookup"><span data-stu-id="cc645-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="cc645-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc645-107">EXAMPLES</span></span>

## <span data-ttu-id="cc645-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc645-108">PARAMETERS</span></span>

### <span data-ttu-id="cc645-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc645-109">-DefaultProfile</span></span>
<span data-ttu-id="cc645-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc645-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc645-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="cc645-111">-Location</span></span>
<span data-ttu-id="cc645-112">A földrajzi hely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc645-112">Specifies the geographical location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc645-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc645-113">-Name</span></span>
<span data-ttu-id="cc645-114">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc645-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc645-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc645-115">-ResourceGroupName</span></span>
<span data-ttu-id="cc645-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc645-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc645-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc645-117">CommonParameters</span></span>
<span data-ttu-id="cc645-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc645-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc645-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc645-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc645-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc645-120">INPUTS</span></span>

### <span data-ttu-id="cc645-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc645-121">None</span></span>
<span data-ttu-id="cc645-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cc645-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc645-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc645-123">OUTPUTS</span></span>

## <span data-ttu-id="cc645-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc645-124">NOTES</span></span>

## <span data-ttu-id="cc645-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc645-125">RELATED LINKS</span></span>

[<span data-ttu-id="cc645-126">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="cc645-126">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="cc645-127">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="cc645-127">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
