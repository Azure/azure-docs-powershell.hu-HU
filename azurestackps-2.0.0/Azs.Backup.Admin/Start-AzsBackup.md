---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844893"
---
# <span data-ttu-id="5423a-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5423a-101">Start-AzsBackup</span></span>

## <span data-ttu-id="5423a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5423a-102">SYNOPSIS</span></span>
<span data-ttu-id="5423a-103">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="5423a-103">Back up a specific location.</span></span>

## <span data-ttu-id="5423a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5423a-104">SYNTAX</span></span>

### <span data-ttu-id="5423a-105">Létrehozás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5423a-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5423a-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5423a-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5423a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5423a-107">DESCRIPTION</span></span>
<span data-ttu-id="5423a-108">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="5423a-108">Back up a specific location.</span></span>

## <span data-ttu-id="5423a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5423a-109">EXAMPLES</span></span>

### <span data-ttu-id="5423a-110">1. példa: azurestack biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="5423a-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="5423a-111">Nyisson meg egy Azure-halom biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="5423a-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="5423a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5423a-112">PARAMETERS</span></span>

### <span data-ttu-id="5423a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5423a-113">-AsJob</span></span>
<span data-ttu-id="5423a-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5423a-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5423a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5423a-115">-DefaultProfile</span></span>
<span data-ttu-id="5423a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5423a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5423a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5423a-117">-InputObject</span></span>
<span data-ttu-id="5423a-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5423a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5423a-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="5423a-119">-Location</span></span>
<span data-ttu-id="5423a-120">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="5423a-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5423a-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="5423a-121">-NoWait</span></span>
<span data-ttu-id="5423a-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5423a-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5423a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5423a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5423a-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5423a-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5423a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5423a-125">-SubscriptionId</span></span>
<span data-ttu-id="5423a-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="5423a-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5423a-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5423a-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5423a-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5423a-128">-Confirm</span></span>
<span data-ttu-id="5423a-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5423a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5423a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5423a-130">-WhatIf</span></span>
<span data-ttu-id="5423a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5423a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5423a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5423a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5423a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5423a-133">CommonParameters</span></span>
<span data-ttu-id="5423a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5423a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5423a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5423a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5423a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5423a-136">INPUTS</span></span>

### <span data-ttu-id="5423a-137">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5423a-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="5423a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5423a-138">OUTPUTS</span></span>

### <span data-ttu-id="5423a-139">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. modellek. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="5423a-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="5423a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5423a-140">NOTES</span></span>

<span data-ttu-id="5423a-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5423a-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5423a-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5423a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5423a-143">INPUTOBJECT <IBackupAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5423a-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5423a-144">`[Backup <String>]`: A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="5423a-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="5423a-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5423a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5423a-146">`[Location <String>]`: A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="5423a-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="5423a-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5423a-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5423a-148">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="5423a-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5423a-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5423a-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5423a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5423a-150">RELATED LINKS</span></span>

