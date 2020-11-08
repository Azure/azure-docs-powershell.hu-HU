---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014708"
---
# <span data-ttu-id="68d08-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="68d08-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="68d08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68d08-102">SYNOPSIS</span></span>
<span data-ttu-id="68d08-103">Ez a parancs elindítja az adott tárolóban lévő adott terhelési típus védtelen elemeinek felderítését.</span><span class="sxs-lookup"><span data-stu-id="68d08-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="68d08-104">Ha az adatbázis-alkalmazás nem az automatikus védelemmel van ellátva, használja ezt a parancsot az új DBs-t a hozzáadásuk után, és folytassa a védelmet.</span><span class="sxs-lookup"><span data-stu-id="68d08-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="68d08-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68d08-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68d08-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="68d08-106">DESCRIPTION</span></span>
<span data-ttu-id="68d08-107">a parancsmag a tárolón belüli bizonyos terhelésekre vonatkozó kérdésekkel kapcsolatos kérdésekről szól.</span><span class="sxs-lookup"><span data-stu-id="68d08-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="68d08-108">Ezzel olyan műveletet indít el, amely védett elemeket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="68d08-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="68d08-109">Példák</span><span class="sxs-lookup"><span data-stu-id="68d08-109">EXAMPLES</span></span>

### <span data-ttu-id="68d08-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68d08-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="68d08-111">A parancsmag az új védett elemek felderítési műveletét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="68d08-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="68d08-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68d08-112">PARAMETERS</span></span>

### <span data-ttu-id="68d08-113">-Container</span><span class="sxs-lookup"><span data-stu-id="68d08-113">-Container</span></span>
<span data-ttu-id="68d08-114">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="68d08-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68d08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d08-115">-DefaultProfile</span></span>
<span data-ttu-id="68d08-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68d08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d08-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68d08-117">-PassThru</span></span>
<span data-ttu-id="68d08-118">Adja vissza a törlendő tárolót.</span><span class="sxs-lookup"><span data-stu-id="68d08-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="68d08-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="68d08-119">-VaultId</span></span>
<span data-ttu-id="68d08-120">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="68d08-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="68d08-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="68d08-121">-WorkloadType</span></span>
<span data-ttu-id="68d08-122">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="68d08-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68d08-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68d08-123">-Confirm</span></span>
<span data-ttu-id="68d08-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68d08-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d08-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d08-125">-WhatIf</span></span>
<span data-ttu-id="68d08-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68d08-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68d08-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68d08-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d08-128">CommonParameters</span></span>
<span data-ttu-id="68d08-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68d08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d08-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="68d08-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d08-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d08-131">INPUTS</span></span>

### <span data-ttu-id="68d08-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="68d08-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="68d08-133">System. String</span><span class="sxs-lookup"><span data-stu-id="68d08-133">System.String</span></span>

## <span data-ttu-id="68d08-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d08-134">OUTPUTS</span></span>

### <span data-ttu-id="68d08-135">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="68d08-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="68d08-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68d08-136">NOTES</span></span>

## <span data-ttu-id="68d08-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68d08-137">RELATED LINKS</span></span>
