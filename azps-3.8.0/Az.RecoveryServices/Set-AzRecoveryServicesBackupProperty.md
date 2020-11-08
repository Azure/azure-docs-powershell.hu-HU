---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 538fe4fe21394c817b7bb2a954fbdbcc2ccfb097
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013525"
---
# <span data-ttu-id="43356-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="43356-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="43356-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43356-102">SYNOPSIS</span></span>
<span data-ttu-id="43356-103">A biztonságimásolat-kezelés tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="43356-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="43356-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43356-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43356-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43356-105">DESCRIPTION</span></span>
<span data-ttu-id="43356-106">A **set-AzRecoveryServicesBackupProperty** parancsmag biztonságimásolat-tárolók tulajdonságait állítja be helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="43356-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="43356-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43356-107">EXAMPLES</span></span>

### <span data-ttu-id="43356-108">1. példa: GeoRedundant-tárterület beállítása a boltozathoz</span><span class="sxs-lookup"><span data-stu-id="43356-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="43356-109">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="43356-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="43356-110">A második parancs a biztonsági másolat tárterületét állítja be a $Vault 01 GeoRedundant-ra.</span><span class="sxs-lookup"><span data-stu-id="43356-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="43356-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43356-111">PARAMETERS</span></span>

### <span data-ttu-id="43356-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="43356-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="43356-113">A biztonsági másolat tárolási redundancia típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="43356-113">Specifies the backup storage redundancy type.</span></span>

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

### <span data-ttu-id="43356-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43356-114">-DefaultProfile</span></span>
<span data-ttu-id="43356-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43356-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43356-116">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="43356-116">-Vault</span></span>
<span data-ttu-id="43356-117">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43356-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="43356-118">A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="43356-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="43356-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43356-119">-Confirm</span></span>
<span data-ttu-id="43356-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43356-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43356-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43356-121">-WhatIf</span></span>
<span data-ttu-id="43356-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43356-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43356-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43356-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43356-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43356-124">CommonParameters</span></span>
<span data-ttu-id="43356-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43356-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43356-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="43356-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43356-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43356-127">INPUTS</span></span>

### <span data-ttu-id="43356-128">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="43356-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="43356-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43356-129">OUTPUTS</span></span>

### <span data-ttu-id="43356-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="43356-130">System.Void</span></span>

## <span data-ttu-id="43356-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43356-131">NOTES</span></span>

## <span data-ttu-id="43356-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43356-132">RELATED LINKS</span></span>

[<span data-ttu-id="43356-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="43356-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="43356-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="43356-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


