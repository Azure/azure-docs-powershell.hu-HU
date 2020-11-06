---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: abc4bce43c5be267e736cb93e03806cdd802fcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493279"
---
# <span data-ttu-id="fbb70-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fbb70-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="fbb70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbb70-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb70-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="fbb70-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbb70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbb70-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb70-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbb70-105">DESCRIPTION</span></span>
<span data-ttu-id="fbb70-106">A **Get-AzureRmBackupContainer** parancsmag Azure Backup-tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="fbb70-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="fbb70-107">Egy **AzureBackupContainer** beágyazza az adatforrásokat, a védett elemeket és a helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="fbb70-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="fbb70-108">Egy **AzureBackupContainer** az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="fbb70-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="fbb70-109">Windows Server rendszerű számítógépen</span><span class="sxs-lookup"><span data-stu-id="fbb70-109">A Windows Server computer</span></span>
- <span data-ttu-id="fbb70-110">A System Center Data Protection Manager (SCDPM) kiszolgálója</span><span class="sxs-lookup"><span data-stu-id="fbb70-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="fbb70-111">Azure-infrastruktúra szolgáltatás (IaaS) virtuális gép</span><span class="sxs-lookup"><span data-stu-id="fbb70-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="fbb70-112">Mielőtt biztonsági másolatot készíthet egy adatforrásról vagy elemről, regisztrálnia kell azt tároló tárolót, amely az Azure Backup szolgáltatással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="fbb70-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="fbb70-113">A tárolónak hitelesítettnek kell lennie, hogy biztonsági másolatot küldjön a biztonságimásolat-tárolónak.</span><span class="sxs-lookup"><span data-stu-id="fbb70-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="fbb70-114">Windows Server rendszerű számítógépek és SCDPM-kiszolgálók esetén a regisztráció a kiszolgáló teljesen minősített tartománynevével történik.</span><span class="sxs-lookup"><span data-stu-id="fbb70-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="fbb70-115">Példák</span><span class="sxs-lookup"><span data-stu-id="fbb70-115">EXAMPLES</span></span>

### <span data-ttu-id="fbb70-116">Példa 1: a boltozathoz regisztrált összes kiszolgáló megtekintése</span><span class="sxs-lookup"><span data-stu-id="fbb70-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="fbb70-117">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="fbb70-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="fbb70-118">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fbb70-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="fbb70-119">A második parancs beolvassa a Windows rendszer minden típusú tárolóját a boltozatról $Vault.</span><span class="sxs-lookup"><span data-stu-id="fbb70-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="fbb70-120">2. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="fbb70-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="fbb70-121">Ez a parancs a DPMSERVER nevű tárolót kapja meg. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="fbb70-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="fbb70-122">A parancs a $Vault és a tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbb70-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="fbb70-123">3. példa: az összes regisztrált Azure virtuális gép megtekintése</span><span class="sxs-lookup"><span data-stu-id="fbb70-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="fbb70-124">Ez a parancs a regisztrált virtuális gépeket az $Vault boltozatáról kapja.</span><span class="sxs-lookup"><span data-stu-id="fbb70-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="fbb70-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbb70-125">PARAMETERS</span></span>

### <span data-ttu-id="fbb70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb70-126">-DefaultProfile</span></span>
<span data-ttu-id="fbb70-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbb70-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbb70-128">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb70-128">-ManagedResourceGroupName</span></span>
<span data-ttu-id="fbb70-129">A tárolóhoz társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbb70-129">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="fbb70-130">Ez a név ugyanazt az értéket adja meg, amelyet az Register-AzureRmBackupContainer parancsmag *szolgáltatásnév* vagy *ResourceGroupName* paramétereként megadott.</span><span class="sxs-lookup"><span data-stu-id="fbb70-130">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb70-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbb70-131">-Name</span></span>
<span data-ttu-id="fbb70-132">Annak a tárolónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="fbb70-132">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb70-133">-Állapot</span><span class="sxs-lookup"><span data-stu-id="fbb70-133">-Status</span></span>
<span data-ttu-id="fbb70-134">A parancsmag által kapott tárolók pillanatnyi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbb70-134">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="fbb70-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fbb70-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbb70-136">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="fbb70-136">NotRegistered</span></span> 
- <span data-ttu-id="fbb70-137">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="fbb70-137">Registered</span></span> 
- <span data-ttu-id="fbb70-138">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="fbb70-138">Registering</span></span>

```yaml
Type: AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb70-139">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="fbb70-139">-Type</span></span>
<span data-ttu-id="fbb70-140">Itt adhatja meg, hogy a parancsmag milyen típusú tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="fbb70-140">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb70-141">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="fbb70-141">-Vault</span></span>
<span data-ttu-id="fbb70-142">A parancsmagot tároló biztonságimásolat-tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbb70-142">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="fbb70-143">Ha **AzureRmBackupVault** szeretne beolvasni, használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fbb70-143">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb70-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb70-144">CommonParameters</span></span>
<span data-ttu-id="fbb70-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbb70-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb70-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb70-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb70-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb70-147">INPUTS</span></span>

### <span data-ttu-id="fbb70-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="fbb70-148">AzureBackupVault</span></span>

## <span data-ttu-id="fbb70-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb70-149">OUTPUTS</span></span>

### <span data-ttu-id="fbb70-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fbb70-150">AzureBackupContainer</span></span>

## <span data-ttu-id="fbb70-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbb70-151">NOTES</span></span>
* <span data-ttu-id="fbb70-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="fbb70-152">None</span></span>

## <span data-ttu-id="fbb70-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbb70-153">RELATED LINKS</span></span>

[<span data-ttu-id="fbb70-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="fbb70-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="fbb70-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fbb70-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="fbb70-156">Regisztráció törlése – AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fbb70-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


