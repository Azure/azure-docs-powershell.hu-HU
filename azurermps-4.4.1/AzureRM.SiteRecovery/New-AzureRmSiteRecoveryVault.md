---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672684"
---
# <span data-ttu-id="26619-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="26619-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="26619-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26619-102">SYNOPSIS</span></span>
<span data-ttu-id="26619-103">Webhely-helyreállítási szolgáltatások boltozatának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="26619-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26619-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26619-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26619-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26619-105">DESCRIPTION</span></span>
<span data-ttu-id="26619-106">A **New-AzureRmSiteRecoveryVault** parancsmag létrehoz egy Azure site Recovery Services Vault-t.</span><span class="sxs-lookup"><span data-stu-id="26619-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="26619-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26619-107">EXAMPLES</span></span>

## <span data-ttu-id="26619-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26619-108">PARAMETERS</span></span>

### <span data-ttu-id="26619-109">-Hely</span><span class="sxs-lookup"><span data-stu-id="26619-109">-Location</span></span>
<span data-ttu-id="26619-110">A földrajzi hely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26619-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26619-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26619-111">-Name</span></span>
<span data-ttu-id="26619-112">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26619-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26619-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26619-113">-ResourceGroupName</span></span>
<span data-ttu-id="26619-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26619-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26619-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26619-115">-DefaultProfile</span></span>
<span data-ttu-id="26619-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26619-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26619-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26619-117">CommonParameters</span></span>
<span data-ttu-id="26619-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26619-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26619-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26619-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26619-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26619-120">INPUTS</span></span>

## <span data-ttu-id="26619-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26619-121">OUTPUTS</span></span>

## <span data-ttu-id="26619-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26619-122">NOTES</span></span>

## <span data-ttu-id="26619-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26619-123">RELATED LINKS</span></span>

[<span data-ttu-id="26619-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="26619-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="26619-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="26619-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
