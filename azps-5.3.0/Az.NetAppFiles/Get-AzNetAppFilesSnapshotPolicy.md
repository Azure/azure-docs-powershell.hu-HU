---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466263"
---
# <span data-ttu-id="21009-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="21009-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="21009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21009-102">SYNOPSIS</span></span>
<span data-ttu-id="21009-103">Részleteket kap az Azure NetApp-fájlok (ANF) pillanatkép-házirendről.</span><span class="sxs-lookup"><span data-stu-id="21009-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="21009-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21009-104">SYNTAX</span></span>

### <span data-ttu-id="21009-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21009-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21009-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21009-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21009-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21009-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21009-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21009-108">DESCRIPTION</span></span>
<span data-ttu-id="21009-109">A **Get-AzNetAppFilesSnapshotPolicy** parancsmag anF-pillanatfelvételi házirend adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="21009-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="21009-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21009-110">EXAMPLES</span></span>

### <span data-ttu-id="21009-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="21009-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="21009-112">Ez a parancs a "MyAnfAccount" fiók "MyBackupPolicy" nevű biztonságimásolat-házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="21009-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="21009-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21009-113">PARAMETERS</span></span>

### <span data-ttu-id="21009-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21009-114">-AccountName</span></span>
<span data-ttu-id="21009-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="21009-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21009-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="21009-116">-AccountObject</span></span>
<span data-ttu-id="21009-117">The Account for the new Snapshot Policy object</span><span class="sxs-lookup"><span data-stu-id="21009-117">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21009-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21009-118">-DefaultProfile</span></span>
<span data-ttu-id="21009-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21009-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21009-120">-Name</span><span class="sxs-lookup"><span data-stu-id="21009-120">-Name</span></span>
<span data-ttu-id="21009-121">Az ANF pillanatkép-házirend neve</span><span class="sxs-lookup"><span data-stu-id="21009-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21009-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21009-122">-ResourceGroupName</span></span>
<span data-ttu-id="21009-123">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="21009-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21009-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21009-124">-ResourceId</span></span>
<span data-ttu-id="21009-125">Az ANF pillanatkép-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="21009-125">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21009-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21009-126">-Confirm</span></span>
<span data-ttu-id="21009-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="21009-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21009-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21009-128">-WhatIf</span></span>
<span data-ttu-id="21009-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="21009-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21009-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21009-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21009-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21009-131">CommonParameters</span></span>
<span data-ttu-id="21009-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21009-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21009-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21009-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21009-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21009-134">INPUTS</span></span>

### <span data-ttu-id="21009-135">System.String</span><span class="sxs-lookup"><span data-stu-id="21009-135">System.String</span></span>

### <span data-ttu-id="21009-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="21009-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="21009-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21009-137">OUTPUTS</span></span>

### <span data-ttu-id="21009-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="21009-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="21009-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21009-139">NOTES</span></span>

## <span data-ttu-id="21009-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21009-140">RELATED LINKS</span></span>
