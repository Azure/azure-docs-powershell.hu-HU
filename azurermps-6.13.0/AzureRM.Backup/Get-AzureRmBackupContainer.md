---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672492"
---
# <span data-ttu-id="14740-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="14740-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="14740-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14740-102">SYNOPSIS</span></span>
<span data-ttu-id="14740-103">Kapja a biztonsági másolat tárolóit.</span><span class="sxs-lookup"><span data-stu-id="14740-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14740-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14740-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14740-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14740-105">DESCRIPTION</span></span>
<span data-ttu-id="14740-106">A **Get-AzureRmBackupContainer** parancsmag Azure Backup-tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="14740-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>
<span data-ttu-id="14740-107">Egy **AzureBackupContainer** beágyazza az adatforrásokat, a védett elemeket és a helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="14740-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="14740-108">Egy **AzureBackupContainer** az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="14740-108">An **AzureBackupContainer** can be one of the following:</span></span> 
- <span data-ttu-id="14740-109">Windows Server rendszerű számítógépen</span><span class="sxs-lookup"><span data-stu-id="14740-109">A Windows Server computer</span></span>
- <span data-ttu-id="14740-110">A System Center Data Protection Manager (SCDPM) kiszolgálója</span><span class="sxs-lookup"><span data-stu-id="14740-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="14740-111">Azure-infrastruktúra szolgáltatásként (IaaS) virtuális gép biztonsági mentése előtt biztonsági másolatot készíthet egy adatforrásról vagy elemről, regisztrálnia kell az azt tároló tárolót, amely az Azure Backup szolgáltatással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="14740-111">An Azure infrastructure as a service (IaaS) virtual machine Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="14740-112">A tárolónak hitelesítettnek kell lennie, hogy biztonsági másolatot küldjön a biztonságimásolat-tárolónak.</span><span class="sxs-lookup"><span data-stu-id="14740-112">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="14740-113">Windows Server rendszerű számítógépek és SCDPM-kiszolgálók esetén a regisztráció a kiszolgáló teljesen minősített tartománynevével történik.</span><span class="sxs-lookup"><span data-stu-id="14740-113">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="14740-114">Példák</span><span class="sxs-lookup"><span data-stu-id="14740-114">EXAMPLES</span></span>

### <span data-ttu-id="14740-115">Példa 1: a boltozathoz regisztrált összes kiszolgáló megtekintése</span><span class="sxs-lookup"><span data-stu-id="14740-115">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="14740-116">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="14740-116">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="14740-117">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="14740-117">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="14740-118">A második parancs beolvassa a Windows rendszer minden típusú tárolóját a boltozatról $Vault.</span><span class="sxs-lookup"><span data-stu-id="14740-118">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="14740-119">2. példa: adott tároló beszerzése</span><span class="sxs-lookup"><span data-stu-id="14740-119">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="14740-120">Ez a parancs a DPMSERVER nevű tárolót kapja meg. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="14740-120">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="14740-121">A parancs a $Vault és a tároló típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14740-121">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="14740-122">3. példa: az összes regisztrált Azure virtuális gép megtekintése</span><span class="sxs-lookup"><span data-stu-id="14740-122">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="14740-123">Ez a parancs a regisztrált virtuális gépeket az $Vault boltozatáról kapja.</span><span class="sxs-lookup"><span data-stu-id="14740-123">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="14740-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14740-124">PARAMETERS</span></span>

### <span data-ttu-id="14740-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14740-125">-DefaultProfile</span></span>
<span data-ttu-id="14740-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="14740-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14740-127">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14740-127">-ManagedResourceGroupName</span></span>
<span data-ttu-id="14740-128">A tárolóhoz társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14740-128">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="14740-129">Ez a név ugyanazt az értéket adja meg, amelyet az Register-AzureRmBackupContainer parancsmag *szolgáltatásnév* vagy *ResourceGroupName* paramétereként megadott.</span><span class="sxs-lookup"><span data-stu-id="14740-129">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="14740-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14740-130">-Name</span></span>
<span data-ttu-id="14740-131">Annak a tárolónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="14740-131">Specifies the name of the container that this cmdlet gets.</span></span>

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

### <span data-ttu-id="14740-132">-Állapot</span><span class="sxs-lookup"><span data-stu-id="14740-132">-Status</span></span>
<span data-ttu-id="14740-133">A parancsmag által kapott tárolók pillanatnyi állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14740-133">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="14740-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="14740-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14740-135">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="14740-135">NotRegistered</span></span> 
- <span data-ttu-id="14740-136">Regisztrált</span><span class="sxs-lookup"><span data-stu-id="14740-136">Registered</span></span> 
- <span data-ttu-id="14740-137">Regisztráció</span><span class="sxs-lookup"><span data-stu-id="14740-137">Registering</span></span>

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

### <span data-ttu-id="14740-138">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="14740-138">-Type</span></span>
<span data-ttu-id="14740-139">Itt adhatja meg, hogy a parancsmag milyen típusú tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="14740-139">Specifies the type of containers that this cmdlet gets.</span></span>

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

### <span data-ttu-id="14740-140">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="14740-140">-Vault</span></span>
<span data-ttu-id="14740-141">A parancsmagot tároló biztonságimásolat-tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="14740-141">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="14740-142">Ha **AzureRmBackupVault** szeretne beolvasni, használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="14740-142">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="14740-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14740-143">CommonParameters</span></span>
<span data-ttu-id="14740-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14740-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14740-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14740-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14740-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14740-146">INPUTS</span></span>

### <span data-ttu-id="14740-147">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="14740-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="14740-148">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14740-148">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="14740-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14740-149">OUTPUTS</span></span>

### <span data-ttu-id="14740-150">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="14740-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>

## <span data-ttu-id="14740-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14740-151">NOTES</span></span>
* <span data-ttu-id="14740-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="14740-152">None</span></span>

## <span data-ttu-id="14740-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14740-153">RELATED LINKS</span></span>

[<span data-ttu-id="14740-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="14740-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="14740-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="14740-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="14740-156">Regisztráció törlése – AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="14740-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


