---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494968"
---
# <span data-ttu-id="d78e0-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="d78e0-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="d78e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d78e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d78e0-103">Biztonsági mentési tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="d78e0-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d78e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d78e0-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d78e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d78e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d78e0-106">A **Get-AzureRmRecoveryServicesBackupProperty** parancsmag biztonsági mentési tulajdonságokat kap a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="d78e0-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="d78e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d78e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d78e0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d78e0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="d78e0-109">A biztonsági másolat boltozat tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d78e0-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="d78e0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d78e0-110">PARAMETERS</span></span>

### <span data-ttu-id="d78e0-111">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="d78e0-111">-Vault</span></span>
<span data-ttu-id="d78e0-112">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d78e0-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="d78e0-113">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d78e0-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d78e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78e0-114">-DefaultProfile</span></span>
<span data-ttu-id="d78e0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d78e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d78e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78e0-116">CommonParameters</span></span>
<span data-ttu-id="d78e0-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d78e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78e0-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d78e0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78e0-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d78e0-119">INPUTS</span></span>

### <span data-ttu-id="d78e0-120">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d78e0-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="d78e0-121">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d78e0-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="d78e0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d78e0-122">OUTPUTS</span></span>

### <span data-ttu-id="d78e0-123">Microsoft. Azure. Command. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="d78e0-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="d78e0-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d78e0-124">NOTES</span></span>

## <span data-ttu-id="d78e0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d78e0-125">RELATED LINKS</span></span>
