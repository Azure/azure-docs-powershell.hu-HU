---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: bd4945436c840323121be7a4450a0042acf67cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151170"
---
# <span data-ttu-id="3ae1c-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3ae1c-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="3ae1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae1c-102">SYNOPSIS</span></span>

<span data-ttu-id="3ae1c-103">Biztonságimásolat-tárolókat kér le.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-103">Gets Backup containers.</span></span>

## <span data-ttu-id="3ae1c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ae1c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae1c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ae1c-105">DESCRIPTION</span></span>

<span data-ttu-id="3ae1c-106">A **Get-AzRecoveryServicesBackupContainer** parancsmag kap egy biztonságimásolat-tárolót.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="3ae1c-107">A biztonsági másolat tárolója biztonsági másolatként modellezett adatforrásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="3ae1c-108">Az "Azure VM" tárolótípus esetén a kimenet felsorolja az összes olyan tárolót, amelynek a neve pontosan egyezik a Friendly Name paraméter értékeként átadott tárolóval.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="3ae1c-109">Más tárolótípusok esetén a kimenet a Rövid név paraméterhez átadott értékhez hasonló nevű tárolók listáját adja eredményként.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="3ae1c-110">Állítsa be a tároló környezetét a -VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="3ae1c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ae1c-111">EXAMPLES</span></span>

### <span data-ttu-id="3ae1c-112">1. példa: Adott tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="3ae1c-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="3ae1c-113">Ez a parancs az AzureVM típusú V2VM nevű tárolót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="3ae1c-114">2. példa: Egy adott típusú összes tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="3ae1c-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="3ae1c-115">Ez a parancs az Azure biztonságimásolat-ügynök által védett összes Windows-tárolót leküldi.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="3ae1c-116">A **BackupManagementType paraméterre** csak Windows-tárolók esetén van szükség.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="3ae1c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ae1c-117">PARAMETERS</span></span>

### <span data-ttu-id="3ae1c-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3ae1c-118">-BackupManagementType</span></span>

<span data-ttu-id="3ae1c-119">A védett erőforrások osztálya.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-119">The class of resources being protected.</span></span> <span data-ttu-id="3ae1c-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3ae1c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ae1c-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3ae1c-121">AzureVM</span></span>
- <span data-ttu-id="3ae1c-122">MARS</span><span class="sxs-lookup"><span data-stu-id="3ae1c-122">MARS</span></span>
- <span data-ttu-id="3ae1c-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="3ae1c-123">AzureWorkload</span></span>
- <span data-ttu-id="3ae1c-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="3ae1c-124">AzureStorage</span></span>

<span data-ttu-id="3ae1c-125">Ez a paraméter megkülönbözteti a MARS ügynökkel vagy más biztonságimásolat-motorokkal készült Windows-gépeket.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="3ae1c-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="3ae1c-126">-ContainerType</span></span>

<span data-ttu-id="3ae1c-127">A biztonsági másolat tárolótípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-127">Specifies the backup container type.</span></span>
<span data-ttu-id="3ae1c-128">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3ae1c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ae1c-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3ae1c-129">AzureVM</span></span>
- <span data-ttu-id="3ae1c-130">Windows</span><span class="sxs-lookup"><span data-stu-id="3ae1c-130">Windows</span></span>
- <span data-ttu-id="3ae1c-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="3ae1c-131">AzureStorage</span></span>
- <span data-ttu-id="3ae1c-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="3ae1c-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="3ae1c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae1c-133">-DefaultProfile</span></span>

<span data-ttu-id="3ae1c-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ae1c-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3ae1c-135">-FriendlyName</span></span>

<span data-ttu-id="3ae1c-136">A lekért tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="3ae1c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae1c-137">-ResourceGroupName</span></span>

<span data-ttu-id="3ae1c-138">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="3ae1c-139">Ez a paraméter csak Azure virtuális gépeken használható.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="3ae1c-140">-Állapot</span><span class="sxs-lookup"><span data-stu-id="3ae1c-140">-Status</span></span>

<span data-ttu-id="3ae1c-141">A tároló regisztrációs állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-141">Specifies the container registration status.</span></span>
<span data-ttu-id="3ae1c-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3ae1c-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ae1c-143">Regisztrálva</span><span class="sxs-lookup"><span data-stu-id="3ae1c-143">Registered</span></span>

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

### <span data-ttu-id="3ae1c-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3ae1c-144">-VaultId</span></span>

<span data-ttu-id="3ae1c-145">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3ae1c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae1c-146">CommonParameters</span></span>
<span data-ttu-id="3ae1c-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae1c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae1c-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ae1c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae1c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ae1c-149">INPUTS</span></span>

### <span data-ttu-id="3ae1c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="3ae1c-150">System.String</span></span>

## <span data-ttu-id="3ae1c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae1c-151">OUTPUTS</span></span>

### <span data-ttu-id="3ae1c-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="3ae1c-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="3ae1c-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ae1c-153">NOTES</span></span>

## <span data-ttu-id="3ae1c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ae1c-154">RELATED LINKS</span></span>

[<span data-ttu-id="3ae1c-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3ae1c-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3ae1c-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="3ae1c-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="3ae1c-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3ae1c-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
