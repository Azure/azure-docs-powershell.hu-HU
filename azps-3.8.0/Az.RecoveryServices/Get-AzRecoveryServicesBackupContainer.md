---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: c7efdf68250b0936ffd62293891eb9ebf47ad833
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010889"
---
# <span data-ttu-id="00fe9-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="00fe9-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="00fe9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00fe9-102">SYNOPSIS</span></span>

<span data-ttu-id="00fe9-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="00fe9-103">Gets Backup containers.</span></span>

## <span data-ttu-id="00fe9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00fe9-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00fe9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00fe9-105">DESCRIPTION</span></span>

<span data-ttu-id="00fe9-106">A **Get-AzRecoveryServicesBackupContainer** parancsmag biztonsági tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="00fe9-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="00fe9-107">A biztonságimásolat-tároló a biztonsági elemekként modellezett adatforrásokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="00fe9-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="00fe9-108">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="00fe9-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="00fe9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="00fe9-109">EXAMPLES</span></span>

### <span data-ttu-id="00fe9-110">1. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="00fe9-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="00fe9-111">Ez a parancs a AzureVM V2VM nevű tárolót kapja.</span><span class="sxs-lookup"><span data-stu-id="00fe9-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="00fe9-112">2. példa: egy adott típus minden tárolójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="00fe9-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="00fe9-113">Ez a parancs az Azure Backup Agent által védett Windows-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="00fe9-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="00fe9-114">A **BackupManagementType** paraméter csak a Windows-tárolók esetében szükséges.</span><span class="sxs-lookup"><span data-stu-id="00fe9-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="00fe9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00fe9-115">PARAMETERS</span></span>

### <span data-ttu-id="00fe9-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="00fe9-116">-BackupManagementType</span></span>

<span data-ttu-id="00fe9-117">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fe9-117">Specifies the backup management type.</span></span>
<span data-ttu-id="00fe9-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="00fe9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00fe9-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="00fe9-119">AzureVM</span></span>
- <span data-ttu-id="00fe9-120">MARS</span><span class="sxs-lookup"><span data-stu-id="00fe9-120">MARS</span></span>
- <span data-ttu-id="00fe9-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="00fe9-121">AzureSQL</span></span>
- <span data-ttu-id="00fe9-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="00fe9-122">AzureStorage</span></span>

<span data-ttu-id="00fe9-123">Ezzel a paraméterrel megkülönböztetheti a MARS-ügynökkel vagy más tartalék motorokkal mentett Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="00fe9-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="00fe9-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="00fe9-124">-ContainerType</span></span>

<span data-ttu-id="00fe9-125">A biztonságimásolat-tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fe9-125">Specifies the backup container type.</span></span>
<span data-ttu-id="00fe9-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="00fe9-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00fe9-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="00fe9-127">AzureVM</span></span>
- <span data-ttu-id="00fe9-128">Windows</span><span class="sxs-lookup"><span data-stu-id="00fe9-128">Windows</span></span>
- <span data-ttu-id="00fe9-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="00fe9-129">AzureSQL</span></span>
- <span data-ttu-id="00fe9-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="00fe9-130">AzureStorage</span></span>
- <span data-ttu-id="00fe9-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="00fe9-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fe9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fe9-132">-DefaultProfile</span></span>

<span data-ttu-id="00fe9-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00fe9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00fe9-134">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="00fe9-134">-FriendlyName</span></span>

<span data-ttu-id="00fe9-135">A beolvasott tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fe9-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="00fe9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fe9-136">-ResourceGroupName</span></span>

<span data-ttu-id="00fe9-137">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fe9-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="00fe9-138">Ez a paraméter csak az Azure Virtual Machines esetén használható.</span><span class="sxs-lookup"><span data-stu-id="00fe9-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="00fe9-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="00fe9-139">-Status</span></span>

<span data-ttu-id="00fe9-140">A tároló regisztrációjának állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fe9-140">Specifies the container registration status.</span></span>
<span data-ttu-id="00fe9-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="00fe9-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00fe9-142">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="00fe9-142">Registered</span></span>

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

### <span data-ttu-id="00fe9-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="00fe9-143">-VaultId</span></span>

<span data-ttu-id="00fe9-144">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="00fe9-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="00fe9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fe9-145">CommonParameters</span></span>
<span data-ttu-id="00fe9-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00fe9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fe9-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="00fe9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fe9-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00fe9-148">INPUTS</span></span>

### <span data-ttu-id="00fe9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="00fe9-149">System.String</span></span>

## <span data-ttu-id="00fe9-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00fe9-150">OUTPUTS</span></span>

### <span data-ttu-id="00fe9-151">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="00fe9-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="00fe9-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00fe9-152">NOTES</span></span>

## <span data-ttu-id="00fe9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00fe9-153">RELATED LINKS</span></span>

[<span data-ttu-id="00fe9-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="00fe9-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="00fe9-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="00fe9-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="00fe9-156">Regisztráció törlése – AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="00fe9-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
