---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926689"
---
# <span data-ttu-id="e1dc4-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e1dc4-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="e1dc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1dc4-103">Frissíti az Azure NetApp-fájlok (ANF) fiókját a megadott opcionális módosítóknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="e1dc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1dc4-104">SYNTAX</span></span>

### <span data-ttu-id="e1dc4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1dc4-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1dc4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1dc4-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1dc4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1dc4-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1dc4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1dc4-108">DESCRIPTION</span></span>
<span data-ttu-id="e1dc4-109">Az **Update-AzNetAppFilesAccount** parancsmag módosítja az ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="e1dc4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1dc4-110">EXAMPLES</span></span>

### <span data-ttu-id="e1dc4-111">1. példa: ANF-fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="e1dc4-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="e1dc4-112">Ez a parancs frissítést hajt végre az adott fiókon, és módosítja a megadott címkéket.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="e1dc4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1dc4-113">PARAMETERS</span></span>

### <span data-ttu-id="e1dc4-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e1dc4-114">-ActiveDirectory</span></span>
<span data-ttu-id="e1dc4-115">Az aktív könyvtárakat képviselő kivonatos tömb</span><span class="sxs-lookup"><span data-stu-id="e1dc4-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="e1dc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1dc4-116">-DefaultProfile</span></span>
<span data-ttu-id="e1dc4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1dc4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1dc4-118">-InputObject</span></span>
<span data-ttu-id="e1dc4-119">Frissítend kell a fiókobjektumot</span><span class="sxs-lookup"><span data-stu-id="e1dc4-119">The account object to update</span></span>

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

### <span data-ttu-id="e1dc4-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e1dc4-120">-Location</span></span>
<span data-ttu-id="e1dc4-121">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="e1dc4-121">The location of the resource</span></span>

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

### <span data-ttu-id="e1dc4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e1dc4-122">-Name</span></span>
<span data-ttu-id="e1dc4-123">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e1dc4-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="e1dc4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1dc4-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1dc4-125">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="e1dc4-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e1dc4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1dc4-126">-ResourceId</span></span>
<span data-ttu-id="e1dc4-127">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e1dc4-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="e1dc4-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1dc4-128">-Tag</span></span>
<span data-ttu-id="e1dc4-129">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="e1dc4-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="e1dc4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1dc4-130">-Confirm</span></span>
<span data-ttu-id="e1dc4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1dc4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1dc4-132">-WhatIf</span></span>
<span data-ttu-id="e1dc4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1dc4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1dc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1dc4-135">CommonParameters</span></span>
<span data-ttu-id="e1dc4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1dc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1dc4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1dc4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1dc4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1dc4-138">INPUTS</span></span>

### <span data-ttu-id="e1dc4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e1dc4-139">System.String</span></span>

### <span data-ttu-id="e1dc4-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e1dc4-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e1dc4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1dc4-141">OUTPUTS</span></span>

### <span data-ttu-id="e1dc4-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e1dc4-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e1dc4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1dc4-143">NOTES</span></span>

## <span data-ttu-id="e1dc4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1dc4-144">RELATED LINKS</span></span>
