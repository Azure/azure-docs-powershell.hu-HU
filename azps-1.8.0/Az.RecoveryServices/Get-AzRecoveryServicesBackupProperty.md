---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 410cd159aacadd83ee03c6e628339be38ca42d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669700"
---
# <span data-ttu-id="80fb3-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="80fb3-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="80fb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="80fb3-103">Biztonsági mentési tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="80fb3-103">Gets Backup properties.</span></span>

## <span data-ttu-id="80fb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80fb3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80fb3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="80fb3-106">A **Get-AzRecoveryServicesBackupProperty** parancsmag biztonsági mentési tulajdonságokat kap a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="80fb3-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="80fb3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="80fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="80fb3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="80fb3-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="80fb3-109">A biztonsági másolat boltozat tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="80fb3-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="80fb3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80fb3-110">PARAMETERS</span></span>

### <span data-ttu-id="80fb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fb3-111">-DefaultProfile</span></span>
<span data-ttu-id="80fb3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80fb3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80fb3-113">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="80fb3-113">-Vault</span></span>
<span data-ttu-id="80fb3-114">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80fb3-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="80fb3-115">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="80fb3-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="80fb3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fb3-116">CommonParameters</span></span>
<span data-ttu-id="80fb3-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80fb3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fb3-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80fb3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fb3-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80fb3-119">INPUTS</span></span>

### <span data-ttu-id="80fb3-120">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="80fb3-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="80fb3-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80fb3-121">OUTPUTS</span></span>

### <span data-ttu-id="80fb3-122">Microsoft. Azure. Command. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="80fb3-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="80fb3-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80fb3-123">NOTES</span></span>

## <span data-ttu-id="80fb3-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80fb3-124">RELATED LINKS</span></span>
