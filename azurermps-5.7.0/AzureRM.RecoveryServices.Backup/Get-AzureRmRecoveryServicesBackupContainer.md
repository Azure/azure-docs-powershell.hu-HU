---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c861c9f18f2fb91838b8e527e2c3ee637098c00a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493079"
---
# <span data-ttu-id="2fee6-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2fee6-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="2fee6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fee6-102">SYNOPSIS</span></span>
<span data-ttu-id="2fee6-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="2fee6-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fee6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fee6-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fee6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fee6-105">DESCRIPTION</span></span>
<span data-ttu-id="2fee6-106">A **Get-AzureRmRecoveryServicesBackupContainer** parancsmag biztonsági tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="2fee6-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="2fee6-107">A biztonságimásolat-tároló a biztonsági elemekként modellezett adatforrásokat ágyazza be.</span><span class="sxs-lookup"><span data-stu-id="2fee6-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="2fee6-108">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="2fee6-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2fee6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2fee6-109">EXAMPLES</span></span>

### <span data-ttu-id="2fee6-110">1. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="2fee6-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="2fee6-111">Ez a parancs a AzureVM V2VM nevű tárolót kapja.</span><span class="sxs-lookup"><span data-stu-id="2fee6-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="2fee6-112">2. példa: egy adott típus minden tárolójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="2fee6-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="2fee6-113">Ez a parancs az Azure Backup Agent által védett Windows-tárolókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="2fee6-114">A *BackupManagementType* paraméter csak a Windows-tárolók esetében szükséges.</span><span class="sxs-lookup"><span data-stu-id="2fee6-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="2fee6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fee6-115">PARAMETERS</span></span>

### <span data-ttu-id="2fee6-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2fee6-116">-BackupManagementType</span></span>
<span data-ttu-id="2fee6-117">A biztonságimásolat-kezelés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-117">Specifies the backup management type.</span></span>
<span data-ttu-id="2fee6-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2fee6-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fee6-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2fee6-119">AzureVM</span></span>
- <span data-ttu-id="2fee6-120">MARS</span><span class="sxs-lookup"><span data-stu-id="2fee6-120">MARS</span></span>
- <span data-ttu-id="2fee6-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="2fee6-121">AzureSQL</span></span>

<span data-ttu-id="2fee6-122">Ezzel a paraméterrel megkülönböztetheti a MARS-ügynökkel vagy más tartalék motorokkal mentett Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="2fee6-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fee6-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="2fee6-123">-ContainerType</span></span>
<span data-ttu-id="2fee6-124">A biztonságimásolat-tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-124">Specifies the backup container type.</span></span>
<span data-ttu-id="2fee6-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2fee6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fee6-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2fee6-126">AzureVM</span></span> 
- <span data-ttu-id="2fee6-127">Windows</span><span class="sxs-lookup"><span data-stu-id="2fee6-127">Windows</span></span>
- <span data-ttu-id="2fee6-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="2fee6-128">AzureSQL</span></span>

```yaml
Type: ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fee6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fee6-129">-DefaultProfile</span></span>
<span data-ttu-id="2fee6-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fee6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fee6-131">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="2fee6-131">-FriendlyName</span></span>
<span data-ttu-id="2fee6-132">A beolvasott tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-132">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fee6-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2fee6-133">-Name</span></span>
<span data-ttu-id="2fee6-134">A beolvasott tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-134">Specifies the name of the container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fee6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fee6-135">-ResourceGroupName</span></span>
<span data-ttu-id="2fee6-136">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="2fee6-137">Ez a paraméter csak az Azure Virtual Machines esetén használható.</span><span class="sxs-lookup"><span data-stu-id="2fee6-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fee6-138">-Állapot</span><span class="sxs-lookup"><span data-stu-id="2fee6-138">-Status</span></span>
<span data-ttu-id="2fee6-139">A tároló regisztrációjának állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fee6-139">Specifies the container registration status.</span></span>
<span data-ttu-id="2fee6-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2fee6-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fee6-141">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="2fee6-141">Registered</span></span>

```yaml
Type: ContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fee6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fee6-142">CommonParameters</span></span>
<span data-ttu-id="2fee6-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fee6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fee6-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fee6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fee6-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fee6-145">INPUTS</span></span>

### <span data-ttu-id="2fee6-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="2fee6-146">None</span></span>
<span data-ttu-id="2fee6-147">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2fee6-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fee6-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fee6-148">OUTPUTS</span></span>

### <span data-ttu-id="2fee6-149">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2fee6-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="2fee6-150">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="2fee6-150">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="2fee6-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fee6-151">NOTES</span></span>

## <span data-ttu-id="2fee6-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fee6-152">RELATED LINKS</span></span>

[<span data-ttu-id="2fee6-153">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2fee6-153">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="2fee6-154">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="2fee6-154">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="2fee6-155">Regisztráció törlése – AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2fee6-155">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


