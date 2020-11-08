---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 27b783234f9f38f7445940ceb9969b6bc7fb6273
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187679"
---
# <span data-ttu-id="14a71-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="14a71-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="14a71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14a71-102">SYNOPSIS</span></span>
<span data-ttu-id="14a71-103">A biztonságimásolat-kezelés tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="14a71-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="14a71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14a71-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14a71-105">DESCRIPTION</span></span>
<span data-ttu-id="14a71-106">A **set-AzRecoveryServicesBackupProperty** parancsmag biztonságimásolat-tárolók tulajdonságait állítja be helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="14a71-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="14a71-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14a71-107">EXAMPLES</span></span>

### <span data-ttu-id="14a71-108">1. példa: GeoRedundant-tárterület beállítása a boltozathoz</span><span class="sxs-lookup"><span data-stu-id="14a71-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="14a71-109">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="14a71-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="14a71-110">A második parancs a biztonsági másolat tárterületét állítja be a $Vault 01 GeoRedundant-ra.</span><span class="sxs-lookup"><span data-stu-id="14a71-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="14a71-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14a71-111">PARAMETERS</span></span>

### <span data-ttu-id="14a71-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="14a71-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="14a71-113">A biztonsági másolat tárolási redundancia típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14a71-113">Specifies the backup storage redundancy type.</span></span>

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

### <span data-ttu-id="14a71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a71-114">-DefaultProfile</span></span>
<span data-ttu-id="14a71-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14a71-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14a71-116">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="14a71-116">-Vault</span></span>
<span data-ttu-id="14a71-117">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14a71-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="14a71-118">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="14a71-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="14a71-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14a71-119">-Confirm</span></span>
<span data-ttu-id="14a71-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14a71-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a71-121">-WhatIf</span></span>
<span data-ttu-id="14a71-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14a71-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="14a71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a71-123">CommonParameters</span></span>
<span data-ttu-id="14a71-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14a71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a71-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14a71-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a71-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14a71-126">INPUTS</span></span>

### <span data-ttu-id="14a71-127">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="14a71-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="14a71-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14a71-128">OUTPUTS</span></span>

### <span data-ttu-id="14a71-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="14a71-129">System.Void</span></span>

## <span data-ttu-id="14a71-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14a71-130">NOTES</span></span>

## <span data-ttu-id="14a71-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14a71-131">RELATED LINKS</span></span>

[<span data-ttu-id="14a71-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="14a71-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="14a71-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="14a71-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

