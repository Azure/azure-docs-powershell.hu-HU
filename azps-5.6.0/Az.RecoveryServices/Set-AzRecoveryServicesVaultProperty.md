---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a88b137b5735984ce6b5f19389d9035b85b1dfe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942234"
---
# <span data-ttu-id="15c6e-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="15c6e-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="15c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="15c6e-103">Frissíti egy tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="15c6e-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="15c6e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15c6e-104">SYNTAX</span></span>

### <span data-ttu-id="15c6e-105">AzureRSVaultSoftDelteParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15c6e-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c6e-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c6e-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c6e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15c6e-107">DESCRIPTION</span></span>
<span data-ttu-id="15c6e-108">A **Set-AzRecoveryServicesVaultProperty** parancsmag frissíti a helyreállítási szolgáltatások tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="15c6e-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="15c6e-109">Ezzel a parancsmaggal engedélyezheti/tilthatja le a szoftveres törlést, vagy beállíthatja a CMK-titkosítást egy két különböző paraméterkészletet is tárolóban.</span><span class="sxs-lookup"><span data-stu-id="15c6e-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="15c6e-110">**A tároló SoftDeleteFeatureState** tulajdonsága csak akkor tiltható le, ha nincsenek regisztrálva tárolók a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="15c6e-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="15c6e-111">AstrustructurEncryption csak akkor beállítható, amikor egy felhasználó először frissíti a CMK-tárolót.</span><span class="sxs-lookup"><span data-stu-id="15c6e-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="15c6e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15c6e-112">EXAMPLES</span></span>

### <span data-ttu-id="15c6e-113">1. példa: Egy tároló SoftDeleteFeatureState frissítése</span><span class="sxs-lookup"><span data-stu-id="15c6e-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="15c6e-114">Az első parancs egy tárolóobjektumot kap, majd a $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="15c6e-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="15c6e-115">A második parancs a tároló SoftDeleteFeatureState tulajdonságát "Engedélyezve" állapotra frissíti.</span><span class="sxs-lookup"><span data-stu-id="15c6e-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="15c6e-116">2. példa: A tároló CMK-titkosításának frissítése</span><span class="sxs-lookup"><span data-stu-id="15c6e-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="15c6e-117">Az első parancsmag megkapja az RSVaultot a titkosítási tulajdonságok frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="15c6e-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="15c6e-118">A második parancsmag megkapja az Azure-kulcs tárolót.</span><span class="sxs-lookup"><span data-stu-id="15c6e-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="15c6e-119">A harmadik parancsmag szerezze be a kulcsot a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="15c6e-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="15c6e-120">A negyedik parancsmag frissíti az ügyfél által felügyelt titkosítási kulcsot az RSVaulton belül.</span><span class="sxs-lookup"><span data-stu-id="15c6e-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="15c6e-121">Az -InfrastructureEncryption paraméter használatával engedélyezheti az infrastruktúra-titkosítást az első frissítéskor.</span><span class="sxs-lookup"><span data-stu-id="15c6e-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="15c6e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15c6e-122">PARAMETERS</span></span>

### <span data-ttu-id="15c6e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c6e-123">-DefaultProfile</span></span>
<span data-ttu-id="15c6e-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15c6e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15c6e-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="15c6e-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="15c6e-126">A Helyreállítási szolgáltatások tároló SoftDeleteFeatureState szolgáltatása.</span><span class="sxs-lookup"><span data-stu-id="15c6e-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c6e-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="15c6e-127">-EncryptionKeyId</span></span>
<span data-ttu-id="15c6e-128">A CMK-hez használt titkosítási kulcs kulcsazonosítója.</span><span class="sxs-lookup"><span data-stu-id="15c6e-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c6e-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15c6e-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="15c6e-130">A kulcstár előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15c6e-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c6e-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="15c6e-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="15c6e-132">Engedélyezi az infrastruktúra-titkosítást ezen a tárolón.</span><span class="sxs-lookup"><span data-stu-id="15c6e-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="15c6e-133">A titkosítás konfigurálásakor engedélyezni kell az infrastruktúra-titkosítást.</span><span class="sxs-lookup"><span data-stu-id="15c6e-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c6e-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="15c6e-134">-VaultId</span></span>
<span data-ttu-id="15c6e-135">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15c6e-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="15c6e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15c6e-136">-Confirm</span></span>
<span data-ttu-id="15c6e-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15c6e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c6e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c6e-138">-WhatIf</span></span>
<span data-ttu-id="15c6e-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15c6e-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="15c6e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c6e-140">CommonParameters</span></span>
<span data-ttu-id="15c6e-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c6e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c6e-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15c6e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c6e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15c6e-143">INPUTS</span></span>

### <span data-ttu-id="15c6e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="15c6e-144">System.String</span></span>

### <span data-ttu-id="15c6e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="15c6e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="15c6e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c6e-146">OUTPUTS</span></span>

### <span data-ttu-id="15c6e-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="15c6e-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="15c6e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15c6e-148">NOTES</span></span>

## <span data-ttu-id="15c6e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15c6e-149">RELATED LINKS</span></span>

[<span data-ttu-id="15c6e-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="15c6e-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="15c6e-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="15c6e-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
