---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494748"
---
# <span data-ttu-id="15733-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="15733-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="15733-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15733-102">SYNOPSIS</span></span>
<span data-ttu-id="15733-103">Lehetővé teszi a biztonsági mentést egy megadott biztonsági házirenddel rendelkező elemhez.</span><span class="sxs-lookup"><span data-stu-id="15733-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15733-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15733-104">SYNTAX</span></span>

### <span data-ttu-id="15733-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15733-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15733-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="15733-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15733-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="15733-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15733-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="15733-108">DESCRIPTION</span></span>
<span data-ttu-id="15733-109">Az **enable-AzureRmRecoveryServicesBackupProtection** parancsmag az Azure Backup Protection házirendjét állítja be egy elemen.</span><span class="sxs-lookup"><span data-stu-id="15733-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="15733-110">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="15733-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="15733-111">Példák</span><span class="sxs-lookup"><span data-stu-id="15733-111">EXAMPLES</span></span>

### <span data-ttu-id="15733-112">1. példa: biztonsági védelem engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="15733-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="15733-113">Az első parancsmag alapértelmezett házirend-objektumot kap, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15733-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="15733-114">A második parancsmag a V2VM nevű ARM virtuális gép biztonsági mentési házirendjét a $Pol házirend segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="15733-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="15733-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15733-115">PARAMETERS</span></span>

### <span data-ttu-id="15733-116">-Elem</span><span class="sxs-lookup"><span data-stu-id="15733-116">-Item</span></span>
<span data-ttu-id="15733-117">Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.</span><span class="sxs-lookup"><span data-stu-id="15733-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="15733-118">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzureRmRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="15733-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15733-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15733-119">-Name</span></span>
<span data-ttu-id="15733-120">A biztonságimásolat-elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15733-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15733-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="15733-121">-Policy</span></span>
<span data-ttu-id="15733-122">Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.</span><span class="sxs-lookup"><span data-stu-id="15733-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="15733-123">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="15733-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15733-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15733-124">-ResourceGroupName</span></span>
<span data-ttu-id="15733-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15733-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="15733-126">Ezt a paramétert csak a ARM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="15733-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15733-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="15733-127">-ServiceName</span></span>
<span data-ttu-id="15733-128">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15733-128">Specifies the service name.</span></span>
<span data-ttu-id="15733-129">Ezt a paramétert csak az ASM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="15733-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15733-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15733-130">-DefaultProfile</span></span>
<span data-ttu-id="15733-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15733-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15733-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15733-132">CommonParameters</span></span>
<span data-ttu-id="15733-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15733-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15733-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15733-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15733-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15733-135">INPUTS</span></span>

### <span data-ttu-id="15733-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="15733-136">ItemBase</span></span>
<span data-ttu-id="15733-137">A "tétel" paraméter értéke az "ItemBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="15733-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="15733-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15733-138">OUTPUTS</span></span>

### <span data-ttu-id="15733-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="15733-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="15733-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15733-140">NOTES</span></span>

## <span data-ttu-id="15733-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15733-141">RELATED LINKS</span></span>

[<span data-ttu-id="15733-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="15733-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="15733-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="15733-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


