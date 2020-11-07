---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679960"
---
# <span data-ttu-id="06380-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="06380-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="06380-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06380-102">SYNOPSIS</span></span>
<span data-ttu-id="06380-103">Beállítja a boltozat kontextusát.</span><span class="sxs-lookup"><span data-stu-id="06380-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06380-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06380-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06380-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06380-105">DESCRIPTION</span></span>
<span data-ttu-id="06380-106">A **set-AzureRmRecoveryServicesVaultContext** parancsmag az Azure webhely-helyreállítási szolgáltatások boltozat-környezetét állítja be.</span><span class="sxs-lookup"><span data-stu-id="06380-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="06380-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06380-107">EXAMPLES</span></span>

## <span data-ttu-id="06380-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06380-108">PARAMETERS</span></span>

### <span data-ttu-id="06380-109">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="06380-109">-Vault</span></span>
<span data-ttu-id="06380-110">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06380-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="06380-111">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="06380-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06380-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06380-112">-DefaultProfile</span></span>
<span data-ttu-id="06380-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06380-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06380-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06380-114">CommonParameters</span></span>
<span data-ttu-id="06380-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06380-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06380-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06380-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06380-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06380-117">INPUTS</span></span>

### <span data-ttu-id="06380-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="06380-118">ARSVault</span></span>
<span data-ttu-id="06380-119">A "Vault" paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="06380-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="06380-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06380-120">OUTPUTS</span></span>

## <span data-ttu-id="06380-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06380-121">NOTES</span></span>

## <span data-ttu-id="06380-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06380-122">RELATED LINKS</span></span>

