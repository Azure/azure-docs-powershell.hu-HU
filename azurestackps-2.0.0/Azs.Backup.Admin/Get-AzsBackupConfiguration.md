---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844906"
---
# <span data-ttu-id="26736-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="26736-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="26736-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26736-102">SYNOPSIS</span></span>
<span data-ttu-id="26736-103">A név alapján megadott biztonsági mentési helyet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="26736-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="26736-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26736-104">SYNTAX</span></span>

### <span data-ttu-id="26736-105">Get (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26736-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26736-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26736-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="26736-107">Lista</span><span class="sxs-lookup"><span data-stu-id="26736-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="26736-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="26736-108">DESCRIPTION</span></span>
<span data-ttu-id="26736-109">A név alapján megadott biztonsági mentési helyet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="26736-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="26736-110">Példák</span><span class="sxs-lookup"><span data-stu-id="26736-110">EXAMPLES</span></span>

### <span data-ttu-id="26736-111">Példa 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="26736-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="26736-112">Azure-halom biztonsági mentése konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="26736-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="26736-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26736-113">PARAMETERS</span></span>

### <span data-ttu-id="26736-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26736-114">-DefaultProfile</span></span>
<span data-ttu-id="26736-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26736-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26736-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26736-116">-InputObject</span></span>
<span data-ttu-id="26736-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26736-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="26736-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="26736-118">-Location</span></span>
<span data-ttu-id="26736-119">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="26736-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26736-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26736-120">-ResourceGroupName</span></span>
<span data-ttu-id="26736-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26736-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="26736-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="26736-122">-Skip</span></span>
<span data-ttu-id="26736-123">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="26736-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="26736-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26736-124">-SubscriptionId</span></span>
<span data-ttu-id="26736-125">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="26736-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="26736-126">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="26736-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="26736-127">-Top</span><span class="sxs-lookup"><span data-stu-id="26736-127">-Top</span></span>
<span data-ttu-id="26736-128">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="26736-128">OData top parameter.</span></span>

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

### <span data-ttu-id="26736-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26736-129">CommonParameters</span></span>
<span data-ttu-id="26736-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26736-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26736-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26736-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26736-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26736-132">INPUTS</span></span>

### <span data-ttu-id="26736-133">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="26736-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="26736-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26736-134">OUTPUTS</span></span>

### <span data-ttu-id="26736-135">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. modellek. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="26736-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="26736-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26736-136">NOTES</span></span>

<span data-ttu-id="26736-137">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="26736-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26736-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="26736-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="26736-139">INPUTOBJECT <IBackupAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="26736-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26736-140">`[Backup <String>]`: A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="26736-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="26736-141">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="26736-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26736-142">`[Location <String>]`: A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="26736-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="26736-143">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26736-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="26736-144">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="26736-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="26736-145">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="26736-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="26736-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26736-146">RELATED LINKS</span></span>

