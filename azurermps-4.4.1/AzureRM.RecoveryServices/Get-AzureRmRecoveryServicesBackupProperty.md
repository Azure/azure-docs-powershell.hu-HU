---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679352"
---
# <span data-ttu-id="22938-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="22938-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="22938-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22938-102">SYNOPSIS</span></span>
<span data-ttu-id="22938-103">Biztonsági mentési tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="22938-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22938-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22938-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22938-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22938-105">DESCRIPTION</span></span>
<span data-ttu-id="22938-106">A **Get-AzureRmRecoveryServicesBackupProperty** parancsmag biztonsági mentési tulajdonságokat kap a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="22938-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="22938-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22938-107">EXAMPLES</span></span>

## <span data-ttu-id="22938-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22938-108">PARAMETERS</span></span>

### <span data-ttu-id="22938-109">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="22938-109">-Vault</span></span>
<span data-ttu-id="22938-110">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22938-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="22938-111">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="22938-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="22938-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22938-112">-DefaultProfile</span></span>
<span data-ttu-id="22938-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22938-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22938-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22938-114">CommonParameters</span></span>
<span data-ttu-id="22938-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22938-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22938-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22938-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22938-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22938-117">INPUTS</span></span>

### <span data-ttu-id="22938-118">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="22938-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="22938-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22938-119">OUTPUTS</span></span>

### <span data-ttu-id="22938-120">Microsoft. Azure. Command. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="22938-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="22938-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22938-121">NOTES</span></span>

## <span data-ttu-id="22938-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22938-122">RELATED LINKS</span></span>

