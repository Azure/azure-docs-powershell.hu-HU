---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669714"
---
# <span data-ttu-id="76e2b-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="76e2b-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="76e2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="76e2b-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="76e2b-103">Gets Backup containers.</span></span>

## <span data-ttu-id="76e2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76e2b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76e2b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76e2b-105">DESCRIPTION</span></span>
<span data-ttu-id="76e2b-106">A **Get-AzRecoveryServicesBackupContainer** parancsmag biztonsági tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="76e2b-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="76e2b-107">A biztonságimásolat-tároló a biztonsági elemekként modellezett adatforrásokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="76e2b-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="76e2b-108">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="76e2b-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="76e2b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76e2b-109">EXAMPLES</span></span>

### <span data-ttu-id="76e2b-110">1. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="76e2b-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="76e2b-111">Ez a parancs a AzureVM V2VM nevű tárolót kapja.</span><span class="sxs-lookup"><span data-stu-id="76e2b-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="76e2b-112">2. példa: egy adott típus minden tárolójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="76e2b-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="76e2b-113">Ez a parancs az Azure Backup Agent által védett Windows-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="76e2b-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="76e2b-114">A *BackupManagementType* paraméter csak a Windows-tárolók esetében szükséges.</span><span class="sxs-lookup"><span data-stu-id="76e2b-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="76e2b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76e2b-115">PARAMETERS</span></span>

### <span data-ttu-id="76e2b-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="76e2b-116">-BackupManagementType</span></span>
<span data-ttu-id="76e2b-117">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e2b-117">Specifies the backup management type.</span></span>
<span data-ttu-id="76e2b-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76e2b-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76e2b-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="76e2b-119">AzureVM</span></span>
- <span data-ttu-id="76e2b-120">MARS</span><span class="sxs-lookup"><span data-stu-id="76e2b-120">MARS</span></span>
- <span data-ttu-id="76e2b-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="76e2b-121">AzureSQL</span></span>
- <span data-ttu-id="76e2b-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="76e2b-122">AzureStorage</span></span>

<span data-ttu-id="76e2b-123">Ezzel a paraméterrel megkülönböztetheti a MARS-ügynökkel vagy más tartalék motorokkal mentett Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="76e2b-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e2b-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="76e2b-124">-ContainerType</span></span>
<span data-ttu-id="76e2b-125">A biztonságimásolat-tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e2b-125">Specifies the backup container type.</span></span>
<span data-ttu-id="76e2b-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76e2b-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76e2b-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="76e2b-127">AzureVM</span></span> 
- <span data-ttu-id="76e2b-128">Windows</span><span class="sxs-lookup"><span data-stu-id="76e2b-128">Windows</span></span>
- <span data-ttu-id="76e2b-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="76e2b-129">AzureSQL</span></span>
- <span data-ttu-id="76e2b-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="76e2b-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e2b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e2b-131">-DefaultProfile</span></span>
<span data-ttu-id="76e2b-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76e2b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e2b-133">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="76e2b-133">-FriendlyName</span></span>
<span data-ttu-id="76e2b-134">A beolvasott tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e2b-134">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e2b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e2b-135">-ResourceGroupName</span></span>
<span data-ttu-id="76e2b-136">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e2b-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="76e2b-137">Ez a paraméter csak az Azure Virtual Machines esetén használható.</span><span class="sxs-lookup"><span data-stu-id="76e2b-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e2b-138">-Állapot</span><span class="sxs-lookup"><span data-stu-id="76e2b-138">-Status</span></span>
<span data-ttu-id="76e2b-139">A tároló regisztrációjának állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e2b-139">Specifies the container registration status.</span></span>
<span data-ttu-id="76e2b-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76e2b-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76e2b-141">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="76e2b-141">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e2b-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="76e2b-142">-VaultId</span></span>
<span data-ttu-id="76e2b-143">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="76e2b-143">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76e2b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e2b-144">CommonParameters</span></span>
<span data-ttu-id="76e2b-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76e2b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e2b-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e2b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e2b-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e2b-147">INPUTS</span></span>

### <span data-ttu-id="76e2b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="76e2b-148">System.String</span></span>

## <span data-ttu-id="76e2b-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e2b-149">OUTPUTS</span></span>

### <span data-ttu-id="76e2b-150">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="76e2b-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="76e2b-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76e2b-151">NOTES</span></span>

## <span data-ttu-id="76e2b-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76e2b-152">RELATED LINKS</span></span>

[<span data-ttu-id="76e2b-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="76e2b-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="76e2b-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="76e2b-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="76e2b-155">Regisztráció törlése – AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="76e2b-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

