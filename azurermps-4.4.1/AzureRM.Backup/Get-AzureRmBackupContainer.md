---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672233"
---
# <span data-ttu-id="2b8a0-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2b8a0-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="2b8a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8a0-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b8a0-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b8a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b8a0-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8a0-106">A **Get-AzureRmBackupContainer** parancsmag Azure Backup-tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="2b8a0-107">Egy **AzureBackupContainer** beágyazza az adatforrásokat, a védett elemeket és a helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="2b8a0-108">Egy **AzureBackupContainer** az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="2b8a0-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="2b8a0-109">Windows Server rendszerű számítógépen</span><span class="sxs-lookup"><span data-stu-id="2b8a0-109">A Windows Server computer</span></span>
- <span data-ttu-id="2b8a0-110">A System Center Data Protection Manager (SCDPM) kiszolgálója</span><span class="sxs-lookup"><span data-stu-id="2b8a0-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="2b8a0-111">Azure-infrastruktúra szolgáltatás (IaaS) virtuális gép</span><span class="sxs-lookup"><span data-stu-id="2b8a0-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="2b8a0-112">Mielőtt biztonsági másolatot készíthet egy adatforrásról vagy elemről, regisztrálnia kell azt tároló tárolót, amely az Azure Backup szolgáltatással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="2b8a0-113">A tárolónak hitelesítettnek kell lennie, hogy biztonsági másolatot küldjön a biztonságimásolat-tárolónak.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="2b8a0-114">Windows Server rendszerű számítógépek és SCDPM-kiszolgálók esetén a regisztráció a kiszolgáló teljesen minősített tartománynevével történik.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="2b8a0-115">Példák</span><span class="sxs-lookup"><span data-stu-id="2b8a0-115">EXAMPLES</span></span>

### <span data-ttu-id="2b8a0-116">Példa 1: a boltozathoz regisztrált összes kiszolgáló megtekintése</span><span class="sxs-lookup"><span data-stu-id="2b8a0-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="2b8a0-117">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="2b8a0-118">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="2b8a0-119">A második parancs beolvassa a Windows rendszer minden típusú tárolóját a boltozatról $Vault.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="2b8a0-120">2. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="2b8a0-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="2b8a0-121">Ez a parancs a DPMSERVER nevű tárolót kapja meg. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="2b8a0-122">A parancs a $Vault és a tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="2b8a0-123">3. példa: az összes regisztrált Azure virtuális gép megtekintése</span><span class="sxs-lookup"><span data-stu-id="2b8a0-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="2b8a0-124">Ez a parancs a regisztrált virtuális gépeket az $Vault boltozatáról kapja.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="2b8a0-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b8a0-125">PARAMETERS</span></span>

### <span data-ttu-id="2b8a0-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b8a0-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="2b8a0-127">A tárolóhoz társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-127">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="2b8a0-128">Ez a név ugyanazt az értéket adja meg, amelyet az Register-AzureRmBackupContainer parancsmag *szolgáltatásnév* vagy *ResourceGroupName* paramétereként megadott.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-128">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8a0-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b8a0-129">-Name</span></span>
<span data-ttu-id="2b8a0-130">Annak a tárolónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-130">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8a0-131">-Állapot</span><span class="sxs-lookup"><span data-stu-id="2b8a0-131">-Status</span></span>
<span data-ttu-id="2b8a0-132">A parancsmag által kapott tárolók pillanatnyi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-132">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="2b8a0-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2b8a0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b8a0-134">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="2b8a0-134">NotRegistered</span></span> 
- <span data-ttu-id="2b8a0-135">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="2b8a0-135">Registered</span></span> 
- <span data-ttu-id="2b8a0-136">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="2b8a0-136">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8a0-137">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="2b8a0-137">-Type</span></span>
<span data-ttu-id="2b8a0-138">Itt adhatja meg, hogy a parancsmag milyen típusú tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-138">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8a0-139">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="2b8a0-139">-Vault</span></span>
<span data-ttu-id="2b8a0-140">A parancsmagot tároló biztonságimásolat-tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-140">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="2b8a0-141">Ha **AzureRmBackupVault** szeretne beolvasni, használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-141">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8a0-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8a0-142">-DefaultProfile</span></span>
<span data-ttu-id="2b8a0-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b8a0-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8a0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8a0-144">CommonParameters</span></span>
<span data-ttu-id="2b8a0-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b8a0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8a0-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8a0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8a0-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b8a0-147">INPUTS</span></span>

### <span data-ttu-id="2b8a0-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="2b8a0-148">AzureBackupVault</span></span>

## <span data-ttu-id="2b8a0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b8a0-149">OUTPUTS</span></span>

### <span data-ttu-id="2b8a0-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2b8a0-150">AzureBackupContainer</span></span>

## <span data-ttu-id="2b8a0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b8a0-151">NOTES</span></span>
* <span data-ttu-id="2b8a0-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b8a0-152">None</span></span>

## <span data-ttu-id="2b8a0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b8a0-153">RELATED LINKS</span></span>

[<span data-ttu-id="2b8a0-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="2b8a0-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="2b8a0-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2b8a0-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="2b8a0-156">Regisztráció törlése – AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2b8a0-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


