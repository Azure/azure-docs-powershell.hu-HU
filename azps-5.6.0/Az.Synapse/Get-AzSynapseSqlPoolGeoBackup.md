---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921546"
---
# <span data-ttu-id="38baf-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="38baf-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="38baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38baf-102">SYNOPSIS</span></span>
<span data-ttu-id="38baf-103">Geodundáns biztonsági másolatot készít egy Sql-készletről.</span><span class="sxs-lookup"><span data-stu-id="38baf-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="38baf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38baf-104">SYNTAX</span></span>

### <span data-ttu-id="38baf-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38baf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38baf-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="38baf-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38baf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38baf-107">DESCRIPTION</span></span>
<span data-ttu-id="38baf-108">A **Get-AzSynapseSqlPoolGeoBackup** parancsmag meghatározott georedundáns biztonsági másolatot kap egy SQL-készletről vagy egy adott munkaterületen rendelkezésre álló georedundáns biztonsági másolatról.</span><span class="sxs-lookup"><span data-stu-id="38baf-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="38baf-109">A georedundáns biztonsági másolat egy különálló földrajzi helyről származó adatfájlokat használó visszaállítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="38baf-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="38baf-110">A Geo-Restore segítségével visszaállíthat egy georedundáns biztonsági másolatot, ha egy regionális kimaradás miatt az SQL-készletet visszaállítja egy új régióba.</span><span class="sxs-lookup"><span data-stu-id="38baf-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="38baf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38baf-111">EXAMPLES</span></span>

### <span data-ttu-id="38baf-112">1. példa: Meghatározott georedundáns biztonsági másolat készítése</span><span class="sxs-lookup"><span data-stu-id="38baf-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="38baf-113">A parancsmag beolvassa a Geo Backup függvényt egy sql-készlethez.</span><span class="sxs-lookup"><span data-stu-id="38baf-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="38baf-114">2. példa: Az összes georedundáns biztonsági másolat lekérte egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="38baf-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="38baf-115">Ez a parancs minden földrajzi redundáns biztonsági mentést elérhetővé válik egy adott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="38baf-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="38baf-116">3. példa: Az összes georedundáns biztonsági másolat behozása egy munkaterületre szűréssel</span><span class="sxs-lookup"><span data-stu-id="38baf-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="38baf-117">Ez a parancs a "Contoso" kezdetű adott munkaterületen elérhető georedundáns biztonsági másolatokat kap.</span><span class="sxs-lookup"><span data-stu-id="38baf-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="38baf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38baf-118">PARAMETERS</span></span>

### <span data-ttu-id="38baf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38baf-119">-DefaultProfile</span></span>
<span data-ttu-id="38baf-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38baf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38baf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38baf-121">-Name</span></span>
<span data-ttu-id="38baf-122">A Synapse Sql-készlet.</span><span class="sxs-lookup"><span data-stu-id="38baf-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38baf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38baf-123">-ResourceId</span></span>
<span data-ttu-id="38baf-124">Sql Pool Geo Backup Resource Id bevitele.</span><span class="sxs-lookup"><span data-stu-id="38baf-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38baf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38baf-125">-ResourceGroupName</span></span>
<span data-ttu-id="38baf-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38baf-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38baf-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38baf-127">-WorkspaceName</span></span>
<span data-ttu-id="38baf-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="38baf-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38baf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38baf-129">CommonParameters</span></span>
<span data-ttu-id="38baf-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38baf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38baf-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38baf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38baf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38baf-132">INPUTS</span></span>

### <span data-ttu-id="38baf-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="38baf-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="38baf-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38baf-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="38baf-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38baf-135">OUTPUTS</span></span>

### <span data-ttu-id="38baf-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="38baf-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="38baf-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38baf-137">NOTES</span></span>

## <span data-ttu-id="38baf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38baf-138">RELATED LINKS</span></span>
