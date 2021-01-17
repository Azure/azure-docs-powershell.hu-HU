---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380490"
---
# <span data-ttu-id="3dd2f-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3dd2f-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="3dd2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd2f-103">Frissíti az Azure NetApp-fájlok (ANF) fiókját a megadott opcionális módosítóknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="3dd2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3dd2f-104">SYNTAX</span></span>

### <span data-ttu-id="3dd2f-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3dd2f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd2f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dd2f-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd2f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dd2f-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd2f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3dd2f-108">DESCRIPTION</span></span>
<span data-ttu-id="3dd2f-109">Az **Update-AzNetAppFilesAccount** parancsmag módosítja az ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="3dd2f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3dd2f-110">EXAMPLES</span></span>

### <span data-ttu-id="3dd2f-111">1. példa: ANF-fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="3dd2f-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="3dd2f-112">Ez a parancs frissítést hajt végre az adott fiókon, és módosítja a megadott címkéket.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="3dd2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dd2f-113">PARAMETERS</span></span>

### <span data-ttu-id="3dd2f-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="3dd2f-114">-ActiveDirectory</span></span>
<span data-ttu-id="3dd2f-115">Az aktív könyvtárakat képviselő kivonatos tömb</span><span class="sxs-lookup"><span data-stu-id="3dd2f-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd2f-116">-DefaultProfile</span></span>
<span data-ttu-id="3dd2f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd2f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dd2f-118">-InputObject</span></span>
<span data-ttu-id="3dd2f-119">Frissítend kell a fiókobjektumot</span><span class="sxs-lookup"><span data-stu-id="3dd2f-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2f-120">-Location</span><span class="sxs-lookup"><span data-stu-id="3dd2f-120">-Location</span></span>
<span data-ttu-id="3dd2f-121">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="3dd2f-121">The location of the resource</span></span>

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

### <span data-ttu-id="3dd2f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3dd2f-122">-Name</span></span>
<span data-ttu-id="3dd2f-123">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="3dd2f-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3dd2f-125">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="3dd2f-125">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dd2f-126">-ResourceId</span></span>
<span data-ttu-id="3dd2f-127">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3dd2f-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="3dd2f-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="3dd2f-128">-Tag</span></span>
<span data-ttu-id="3dd2f-129">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="3dd2f-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd2f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dd2f-130">-Confirm</span></span>
<span data-ttu-id="3dd2f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd2f-132">-WhatIf</span></span>
<span data-ttu-id="3dd2f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd2f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd2f-135">CommonParameters</span></span>
<span data-ttu-id="3dd2f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd2f-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dd2f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd2f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3dd2f-138">INPUTS</span></span>

### <span data-ttu-id="3dd2f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3dd2f-139">System.String</span></span>

### <span data-ttu-id="3dd2f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3dd2f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="3dd2f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dd2f-141">OUTPUTS</span></span>

### <span data-ttu-id="3dd2f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3dd2f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="3dd2f-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3dd2f-143">NOTES</span></span>

## <span data-ttu-id="3dd2f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dd2f-144">RELATED LINKS</span></span>
