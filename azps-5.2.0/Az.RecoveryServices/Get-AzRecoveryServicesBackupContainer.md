---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358803"
---
# <span data-ttu-id="92480-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="92480-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="92480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92480-102">SYNOPSIS</span></span>

<span data-ttu-id="92480-103">Biztonságimásolat-tárolókat kér le.</span><span class="sxs-lookup"><span data-stu-id="92480-103">Gets Backup containers.</span></span>

## <span data-ttu-id="92480-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92480-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92480-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92480-105">DESCRIPTION</span></span>

<span data-ttu-id="92480-106">A **Get-AzRecoveryServicesBackupContainer** parancsmag kap egy biztonságimásolat-tárolót.</span><span class="sxs-lookup"><span data-stu-id="92480-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="92480-107">A biztonsági másolat tárolója biztonsági másolatként modellezett adatforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="92480-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="92480-108">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="92480-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="92480-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92480-109">EXAMPLES</span></span>

### <span data-ttu-id="92480-110">1. példa: Adott tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="92480-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="92480-111">Ez a parancs az AzureVM típusú V2VM nevű tárolót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92480-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="92480-112">2. példa: Egy adott típusú összes tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="92480-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="92480-113">Ez a parancs az Azure biztonságimásolat-ügynök által védett összes Windows-tárolót leküldi.</span><span class="sxs-lookup"><span data-stu-id="92480-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="92480-114">A **BackupManagementType paraméterre** csak Windows-tárolók esetén van szükség.</span><span class="sxs-lookup"><span data-stu-id="92480-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="92480-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92480-115">PARAMETERS</span></span>

### <span data-ttu-id="92480-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="92480-116">-BackupManagementType</span></span>

<span data-ttu-id="92480-117">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="92480-117">The class of resources being protected.</span></span> <span data-ttu-id="92480-118">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="92480-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92480-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="92480-119">AzureVM</span></span>
- <span data-ttu-id="92480-120">MARS</span><span class="sxs-lookup"><span data-stu-id="92480-120">MARS</span></span>
- <span data-ttu-id="92480-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="92480-121">AzureWorkload</span></span>
- <span data-ttu-id="92480-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="92480-122">AzureStorage</span></span>

<span data-ttu-id="92480-123">Ez a paraméter megkülönbözteti a MARS ügynökkel vagy más biztonságimásolat-motorokkal készült Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="92480-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="92480-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="92480-124">-ContainerType</span></span>

<span data-ttu-id="92480-125">A biztonsági másolat tárolótípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="92480-125">Specifies the backup container type.</span></span>
<span data-ttu-id="92480-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="92480-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92480-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="92480-127">AzureVM</span></span>
- <span data-ttu-id="92480-128">Windows</span><span class="sxs-lookup"><span data-stu-id="92480-128">Windows</span></span>
- <span data-ttu-id="92480-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="92480-129">AzureSQL</span></span>
- <span data-ttu-id="92480-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="92480-130">AzureStorage</span></span>
- <span data-ttu-id="92480-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="92480-131">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="92480-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92480-132">-DefaultProfile</span></span>

<span data-ttu-id="92480-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92480-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92480-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="92480-134">-FriendlyName</span></span>

<span data-ttu-id="92480-135">A lekért tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92480-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="92480-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92480-136">-ResourceGroupName</span></span>

<span data-ttu-id="92480-137">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92480-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="92480-138">Ez a paraméter csak Azure virtuális gépeken használható.</span><span class="sxs-lookup"><span data-stu-id="92480-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="92480-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="92480-139">-Status</span></span>

<span data-ttu-id="92480-140">A tároló regisztrációs állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="92480-140">Specifies the container registration status.</span></span>
<span data-ttu-id="92480-141">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="92480-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92480-142">Regisztrálva</span><span class="sxs-lookup"><span data-stu-id="92480-142">Registered</span></span>

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

### <span data-ttu-id="92480-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="92480-143">-VaultId</span></span>

<span data-ttu-id="92480-144">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92480-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="92480-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92480-145">CommonParameters</span></span>
<span data-ttu-id="92480-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92480-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92480-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92480-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92480-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92480-148">INPUTS</span></span>

### <span data-ttu-id="92480-149">System.String</span><span class="sxs-lookup"><span data-stu-id="92480-149">System.String</span></span>

## <span data-ttu-id="92480-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92480-150">OUTPUTS</span></span>

### <span data-ttu-id="92480-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="92480-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="92480-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92480-152">NOTES</span></span>

## <span data-ttu-id="92480-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92480-153">RELATED LINKS</span></span>

[<span data-ttu-id="92480-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="92480-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="92480-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="92480-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="92480-156">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="92480-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
