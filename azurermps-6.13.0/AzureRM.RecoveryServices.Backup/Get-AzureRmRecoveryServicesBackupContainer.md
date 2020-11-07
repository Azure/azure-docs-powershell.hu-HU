---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679527"
---
# <span data-ttu-id="59fc3-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59fc3-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="59fc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="59fc3-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="59fc3-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59fc3-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59fc3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="59fc3-106">A **Get-AzureRmRecoveryServicesBackupContainer** parancsmag biztonsági tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="59fc3-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="59fc3-107">A biztonságimásolat-tároló a biztonsági elemekként modellezett adatforrásokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="59fc3-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="59fc3-108">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="59fc3-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="59fc3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="59fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="59fc3-110">1. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="59fc3-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="59fc3-111">Ez a parancs a AzureVM V2VM nevű tárolót kapja.</span><span class="sxs-lookup"><span data-stu-id="59fc3-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="59fc3-112">2. példa: egy adott típus minden tárolójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="59fc3-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="59fc3-113">Ez a parancs az Azure Backup Agent által védett Windows-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="59fc3-114">A *BackupManagementType* paraméter csak a Windows-tárolók esetében szükséges.</span><span class="sxs-lookup"><span data-stu-id="59fc3-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="59fc3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59fc3-115">PARAMETERS</span></span>

### <span data-ttu-id="59fc3-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="59fc3-116">-BackupManagementType</span></span>
<span data-ttu-id="59fc3-117">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-117">Specifies the backup management type.</span></span>
<span data-ttu-id="59fc3-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fc3-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fc3-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="59fc3-119">AzureVM</span></span>
- <span data-ttu-id="59fc3-120">MARS</span><span class="sxs-lookup"><span data-stu-id="59fc3-120">MARS</span></span>
- <span data-ttu-id="59fc3-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="59fc3-121">AzureSQL</span></span>
- <span data-ttu-id="59fc3-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="59fc3-122">AzureStorage</span></span>

<span data-ttu-id="59fc3-123">Ezzel a paraméterrel megkülönböztetheti a MARS-ügynökkel vagy más tartalék motorokkal mentett Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="59fc3-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="59fc3-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="59fc3-124">-ContainerType</span></span>
<span data-ttu-id="59fc3-125">A biztonságimásolat-tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-125">Specifies the backup container type.</span></span>
<span data-ttu-id="59fc3-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fc3-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fc3-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="59fc3-127">AzureVM</span></span> 
- <span data-ttu-id="59fc3-128">Windows</span><span class="sxs-lookup"><span data-stu-id="59fc3-128">Windows</span></span>
- <span data-ttu-id="59fc3-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="59fc3-129">AzureSQL</span></span>
- <span data-ttu-id="59fc3-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="59fc3-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fc3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fc3-131">-DefaultProfile</span></span>
<span data-ttu-id="59fc3-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59fc3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59fc3-133">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="59fc3-133">-FriendlyName</span></span>
<span data-ttu-id="59fc3-134">A beolvasott tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="59fc3-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59fc3-135">-Name</span></span>
<span data-ttu-id="59fc3-136">A beolvasott tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="59fc3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fc3-137">-ResourceGroupName</span></span>
<span data-ttu-id="59fc3-138">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="59fc3-139">Ez a paraméter csak az Azure Virtual Machines esetén használható.</span><span class="sxs-lookup"><span data-stu-id="59fc3-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="59fc3-140">-Állapot</span><span class="sxs-lookup"><span data-stu-id="59fc3-140">-Status</span></span>
<span data-ttu-id="59fc3-141">A tároló regisztrációjának állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59fc3-141">Specifies the container registration status.</span></span>
<span data-ttu-id="59fc3-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="59fc3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fc3-143">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="59fc3-143">Registered</span></span>

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

### <span data-ttu-id="59fc3-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="59fc3-144">-VaultId</span></span>
<span data-ttu-id="59fc3-145">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="59fc3-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="59fc3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fc3-146">CommonParameters</span></span>
<span data-ttu-id="59fc3-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59fc3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fc3-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fc3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fc3-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59fc3-149">INPUTS</span></span>

### <span data-ttu-id="59fc3-150">System. String</span><span class="sxs-lookup"><span data-stu-id="59fc3-150">System.String</span></span>
<span data-ttu-id="59fc3-151">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59fc3-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="59fc3-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59fc3-152">OUTPUTS</span></span>

### <span data-ttu-id="59fc3-153">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="59fc3-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="59fc3-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59fc3-154">NOTES</span></span>

## <span data-ttu-id="59fc3-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59fc3-155">RELATED LINKS</span></span>

[<span data-ttu-id="59fc3-156">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="59fc3-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="59fc3-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="59fc3-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="59fc3-158">Regisztráció törlése – AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59fc3-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


