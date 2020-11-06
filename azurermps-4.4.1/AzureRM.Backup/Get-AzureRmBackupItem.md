---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493576"
---
# <span data-ttu-id="36c44-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="36c44-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="36c44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36c44-102">SYNOPSIS</span></span>
<span data-ttu-id="36c44-103">Egy tárolóban lévő elemek beolvasása biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="36c44-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36c44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36c44-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36c44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36c44-105">DESCRIPTION</span></span>
<span data-ttu-id="36c44-106">A **Get-AzureRmBackupItem** parancsmag az Azure biztonsági másolatban szereplő elemeket, illetve az elemek védelmi állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="36c44-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="36c44-107">A Enable-AzureRmBackupProtection parancsmag használatával védelmet engedélyezhet az elemek számára.</span><span class="sxs-lookup"><span data-stu-id="36c44-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="36c44-108">A biztonságimásolat-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.</span><span class="sxs-lookup"><span data-stu-id="36c44-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="36c44-109">Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy elem lehet.</span><span class="sxs-lookup"><span data-stu-id="36c44-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="36c44-110">Példák</span><span class="sxs-lookup"><span data-stu-id="36c44-110">EXAMPLES</span></span>

### <span data-ttu-id="36c44-111">1. példa: a tároló elemeinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="36c44-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="36c44-112">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="36c44-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="36c44-113">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="36c44-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="36c44-114">A második parancs a **Get-AzureRmBackupContainer** parancsmaggal egy olyan tárolót kap, amelyben a megadott név szerepel a boltozaton $Vault.</span><span class="sxs-lookup"><span data-stu-id="36c44-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="36c44-115">A parancs az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="36c44-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="36c44-116">A végleges parancs a biztonsági másolat elemet kapja meg a tárolóban a $Containerban.</span><span class="sxs-lookup"><span data-stu-id="36c44-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="36c44-117">2. példa: egy elem összes tulajdonságának megtekintése</span><span class="sxs-lookup"><span data-stu-id="36c44-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="36c44-118">Ez a parancs beilleszti a biztonsági másolatot a tárolóba $Container, majd átadja a Select-Object parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="36c44-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="36c44-119">Ez a parancsmag a biztonságimásolat-elem összes tulajdonságát visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="36c44-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="36c44-120">További információért írja be a következőt: `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="36c44-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="36c44-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36c44-121">PARAMETERS</span></span>

### <span data-ttu-id="36c44-122">-Container</span><span class="sxs-lookup"><span data-stu-id="36c44-122">-Container</span></span>
<span data-ttu-id="36c44-123">Annak a tároló objektumnak a megadása, amelyhez a parancsmag biztonsági elemeket kap.</span><span class="sxs-lookup"><span data-stu-id="36c44-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="36c44-124">Ha **AzureRmBackupContainer** szeretne beolvasni, használja az Get-AzureRmBackupContainer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="36c44-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-125">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="36c44-125">-ProtectionStatus</span></span>
<span data-ttu-id="36c44-126">A tároló elemeinek általános védelmi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="36c44-126">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="36c44-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="36c44-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36c44-128">Védett</span><span class="sxs-lookup"><span data-stu-id="36c44-128">Protected</span></span> 
- <span data-ttu-id="36c44-129">Védelme</span><span class="sxs-lookup"><span data-stu-id="36c44-129">Protecting</span></span>  
- <span data-ttu-id="36c44-130">NotProtected</span><span class="sxs-lookup"><span data-stu-id="36c44-130">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-131">-Állapot</span><span class="sxs-lookup"><span data-stu-id="36c44-131">-Status</span></span>
<span data-ttu-id="36c44-132">Egy elem biztonsági állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="36c44-132">Specifies the backup status for an item.</span></span>
<span data-ttu-id="36c44-133">A paraméter elfogadható értékei a következők: IRPending, védett, ProtectionError és ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="36c44-133">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="36c44-134">Ha a *ProtectionStatus* paraméter védett értékkel rendelkezik, az *állapot* paraméter értékét használhatja az elemek szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="36c44-134">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-135">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="36c44-135">-Type</span></span>
<span data-ttu-id="36c44-136">Annak az elemnek a típusa, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="36c44-136">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="36c44-137">Jelenleg az egyetlen támogatott érték a AzureVM.</span><span class="sxs-lookup"><span data-stu-id="36c44-137">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c44-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c44-138">-DefaultProfile</span></span>
<span data-ttu-id="36c44-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36c44-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36c44-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c44-140">CommonParameters</span></span>
<span data-ttu-id="36c44-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36c44-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c44-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c44-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c44-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36c44-143">INPUTS</span></span>

### <span data-ttu-id="36c44-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="36c44-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="36c44-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36c44-145">OUTPUTS</span></span>

### <span data-ttu-id="36c44-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="36c44-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="36c44-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36c44-147">NOTES</span></span>

## <span data-ttu-id="36c44-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36c44-148">RELATED LINKS</span></span>

[<span data-ttu-id="36c44-149">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="36c44-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="36c44-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="36c44-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="36c44-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="36c44-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="36c44-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="36c44-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="36c44-153">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="36c44-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="36c44-154">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="36c44-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


