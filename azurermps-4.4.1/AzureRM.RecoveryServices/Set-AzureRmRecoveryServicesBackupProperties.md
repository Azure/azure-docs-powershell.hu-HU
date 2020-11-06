---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: bb4009edce4e447daacd4cd32835bebc8655dba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494726"
---
# <span data-ttu-id="07298-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="07298-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="07298-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07298-102">SYNOPSIS</span></span>
<span data-ttu-id="07298-103">A biztonságimásolat-kezelés tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="07298-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07298-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07298-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07298-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07298-105">DESCRIPTION</span></span>
<span data-ttu-id="07298-106">A **set-AzureRmRecoveryServicesBackupProperties** parancsmag biztonságimásolat-tárolók tulajdonságait állítja be helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="07298-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="07298-107">Példák</span><span class="sxs-lookup"><span data-stu-id="07298-107">EXAMPLES</span></span>

### <span data-ttu-id="07298-108">1. példa: GeoRedundant-tárterület beállítása a boltozathoz</span><span class="sxs-lookup"><span data-stu-id="07298-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="07298-109">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="07298-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="07298-110">A második parancs a biztonsági másolat tárterületét állítja be a $Vault 01 GeoRedundant-ra.</span><span class="sxs-lookup"><span data-stu-id="07298-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="07298-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07298-111">PARAMETERS</span></span>

### <span data-ttu-id="07298-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="07298-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="07298-113">A biztonsági másolat tárolási redundancia típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07298-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07298-114">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="07298-114">-Vault</span></span>
<span data-ttu-id="07298-115">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07298-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="07298-116">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="07298-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="07298-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07298-117">-Confirm</span></span>
<span data-ttu-id="07298-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07298-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07298-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07298-119">-WhatIf</span></span>
<span data-ttu-id="07298-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07298-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07298-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07298-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07298-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07298-122">-DefaultProfile</span></span>
<span data-ttu-id="07298-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07298-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07298-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07298-124">CommonParameters</span></span>
<span data-ttu-id="07298-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07298-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07298-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07298-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07298-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07298-127">INPUTS</span></span>

### <span data-ttu-id="07298-128">ARSVault</span><span class="sxs-lookup"><span data-stu-id="07298-128">ARSVault</span></span>
<span data-ttu-id="07298-129">A "Vault" paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="07298-129">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="07298-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07298-130">OUTPUTS</span></span>

## <span data-ttu-id="07298-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07298-131">NOTES</span></span>

## <span data-ttu-id="07298-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07298-132">RELATED LINKS</span></span>

[<span data-ttu-id="07298-133">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="07298-133">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="07298-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="07298-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


