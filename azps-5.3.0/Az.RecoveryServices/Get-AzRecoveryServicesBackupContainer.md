---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 90532c6d314c78e6b7242ec480b95991138719de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476726"
---
# <span data-ttu-id="a400b-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a400b-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="a400b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a400b-102">SYNOPSIS</span></span>

<span data-ttu-id="a400b-103">Biztonságimásolat-tárolókat kér le.</span><span class="sxs-lookup"><span data-stu-id="a400b-103">Gets Backup containers.</span></span>

## <span data-ttu-id="a400b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a400b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a400b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a400b-105">DESCRIPTION</span></span>

<span data-ttu-id="a400b-106">A **Get-AzRecoveryServicesBackupContainer** parancsmag kap egy biztonságimásolat-tárolót.</span><span class="sxs-lookup"><span data-stu-id="a400b-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="a400b-107">A biztonsági másolat tárolója biztonsági másolatként modellezett adatforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a400b-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="a400b-108">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="a400b-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="a400b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a400b-109">EXAMPLES</span></span>

### <span data-ttu-id="a400b-110">1. példa: Adott tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="a400b-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="a400b-111">Ez a parancs az AzureVM típusú V2VM nevű tárolót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a400b-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="a400b-112">2. példa: Egy adott típusú összes tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="a400b-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="a400b-113">Ez a parancs az Azure biztonságimásolat-ügynök által védett összes Windows-tárolót leküldi.</span><span class="sxs-lookup"><span data-stu-id="a400b-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="a400b-114">A **BackupManagementType paraméterre** csak Windows-tárolók esetén van szükség.</span><span class="sxs-lookup"><span data-stu-id="a400b-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="a400b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a400b-115">PARAMETERS</span></span>

### <span data-ttu-id="a400b-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a400b-116">-BackupManagementType</span></span>

<span data-ttu-id="a400b-117">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="a400b-117">The class of resources being protected.</span></span> <span data-ttu-id="a400b-118">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="a400b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a400b-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a400b-119">AzureVM</span></span>
- <span data-ttu-id="a400b-120">MARS</span><span class="sxs-lookup"><span data-stu-id="a400b-120">MARS</span></span>
- <span data-ttu-id="a400b-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="a400b-121">AzureWorkload</span></span>
- <span data-ttu-id="a400b-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="a400b-122">AzureStorage</span></span>

<span data-ttu-id="a400b-123">Ez a paraméter megkülönbözteti a MARS ügynökkel vagy más biztonságimásolat-motorokkal készült Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="a400b-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a400b-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="a400b-124">-ContainerType</span></span>

<span data-ttu-id="a400b-125">A biztonsági másolat tárolótípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a400b-125">Specifies the backup container type.</span></span>
<span data-ttu-id="a400b-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="a400b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a400b-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a400b-127">AzureVM</span></span>
- <span data-ttu-id="a400b-128">Windows</span><span class="sxs-lookup"><span data-stu-id="a400b-128">Windows</span></span>
- <span data-ttu-id="a400b-129">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="a400b-129">AzureStorage</span></span>
- <span data-ttu-id="a400b-130">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="a400b-130">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a400b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a400b-131">-DefaultProfile</span></span>

<span data-ttu-id="a400b-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a400b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a400b-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a400b-133">-FriendlyName</span></span>

<span data-ttu-id="a400b-134">A lekért tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a400b-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="a400b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a400b-135">-ResourceGroupName</span></span>

<span data-ttu-id="a400b-136">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a400b-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="a400b-137">Ez a paraméter csak Azure virtuális gépeken használható.</span><span class="sxs-lookup"><span data-stu-id="a400b-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="a400b-138">-Állapot</span><span class="sxs-lookup"><span data-stu-id="a400b-138">-Status</span></span>

<span data-ttu-id="a400b-139">A tároló regisztrációs állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a400b-139">Specifies the container registration status.</span></span>
<span data-ttu-id="a400b-140">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="a400b-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a400b-141">Regisztrálva</span><span class="sxs-lookup"><span data-stu-id="a400b-141">Registered</span></span>

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

### <span data-ttu-id="a400b-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a400b-142">-VaultId</span></span>

<span data-ttu-id="a400b-143">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a400b-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a400b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a400b-144">CommonParameters</span></span>
<span data-ttu-id="a400b-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a400b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a400b-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a400b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a400b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a400b-147">INPUTS</span></span>

### <span data-ttu-id="a400b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a400b-148">System.String</span></span>

## <span data-ttu-id="a400b-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a400b-149">OUTPUTS</span></span>

### <span data-ttu-id="a400b-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="a400b-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="a400b-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a400b-151">NOTES</span></span>

## <span data-ttu-id="a400b-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a400b-152">RELATED LINKS</span></span>

[<span data-ttu-id="a400b-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a400b-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a400b-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="a400b-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="a400b-155">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a400b-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
