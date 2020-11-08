---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017134"
---
# <span data-ttu-id="1401b-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1401b-101">Get-AzsBackup</span></span>

## <span data-ttu-id="1401b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1401b-102">SYNOPSIS</span></span>
<span data-ttu-id="1401b-103">A név alapján kapott hely biztonsági másolatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1401b-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="1401b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1401b-104">SYNTAX</span></span>

### <span data-ttu-id="1401b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1401b-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1401b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1401b-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1401b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1401b-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1401b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1401b-108">DESCRIPTION</span></span>
<span data-ttu-id="1401b-109">A név alapján kapott hely biztonsági másolatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1401b-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="1401b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1401b-110">EXAMPLES</span></span>

### <span data-ttu-id="1401b-111">1. példa: biztonsági másolatok listája</span><span class="sxs-lookup"><span data-stu-id="1401b-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="1401b-112">Információkat kaphat az Azure sbout minden biztonsági mentéséről.</span><span class="sxs-lookup"><span data-stu-id="1401b-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="1401b-113">2. példa: speciális biztonsági másolat kérése</span><span class="sxs-lookup"><span data-stu-id="1401b-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="1401b-114">Információkat kaphat a megadott Azure-halom biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="1401b-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="1401b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1401b-115">PARAMETERS</span></span>

### <span data-ttu-id="1401b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1401b-116">-DefaultProfile</span></span>
<span data-ttu-id="1401b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1401b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1401b-118">-InputObject</span></span>
<span data-ttu-id="1401b-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1401b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="1401b-120">-Location</span></span>
<span data-ttu-id="1401b-121">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="1401b-121">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1401b-122">-Name</span></span>
<span data-ttu-id="1401b-123">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="1401b-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1401b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1401b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1401b-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="1401b-126">-Skip</span></span>
<span data-ttu-id="1401b-127">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="1401b-127">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1401b-128">-SubscriptionId</span></span>
<span data-ttu-id="1401b-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1401b-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1401b-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1401b-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-131">-Top</span><span class="sxs-lookup"><span data-stu-id="1401b-131">-Top</span></span>
<span data-ttu-id="1401b-132">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="1401b-132">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1401b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1401b-133">CommonParameters</span></span>
<span data-ttu-id="1401b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1401b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1401b-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1401b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1401b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1401b-136">INPUTS</span></span>

### <span data-ttu-id="1401b-137">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1401b-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="1401b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1401b-138">OUTPUTS</span></span>

### <span data-ttu-id="1401b-139">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. modellek. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="1401b-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="1401b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1401b-140">NOTES</span></span>

<span data-ttu-id="1401b-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1401b-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1401b-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1401b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1401b-143">INPUTOBJECT <IBackupAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1401b-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1401b-144">`[Backup <String>]`: A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="1401b-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="1401b-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1401b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1401b-146">`[Location <String>]`: A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="1401b-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="1401b-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1401b-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1401b-148">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1401b-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1401b-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1401b-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1401b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1401b-150">RELATED LINKS</span></span>

