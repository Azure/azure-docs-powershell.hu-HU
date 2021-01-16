---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380517"
---
# <span data-ttu-id="887bb-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="887bb-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="887bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="887bb-102">SYNOPSIS</span></span>
<span data-ttu-id="887bb-103">Frissíti az Azure NetApp-fájlok (ANF) fiókját az új adatkészletekkel.</span><span class="sxs-lookup"><span data-stu-id="887bb-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="887bb-104">A társított aktív címtárak törlésekor lehet hasznos.</span><span class="sxs-lookup"><span data-stu-id="887bb-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="887bb-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="887bb-105">SYNTAX</span></span>

### <span data-ttu-id="887bb-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="887bb-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887bb-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="887bb-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887bb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="887bb-108">DESCRIPTION</span></span>
<span data-ttu-id="887bb-109">A **Set-AzNetAppFilesAccount** parancsmag módosítja az ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="887bb-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="887bb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="887bb-110">EXAMPLES</span></span>

### <span data-ttu-id="887bb-111">1. példa: ANF-fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="887bb-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="887bb-112">Ez a parancs frissítést hajt végre az adott fiókon.</span><span class="sxs-lookup"><span data-stu-id="887bb-112">This command performs an update on the given account.</span></span> <span data-ttu-id="887bb-113">Az Active Directory hiánya azt jelenti, hogy az törlődik a fiókból.</span><span class="sxs-lookup"><span data-stu-id="887bb-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="887bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="887bb-114">PARAMETERS</span></span>

### <span data-ttu-id="887bb-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="887bb-115">-ActiveDirectory</span></span>
<span data-ttu-id="887bb-116">Az aktív könyvtárakat képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="887bb-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887bb-117">-DefaultProfile</span></span>
<span data-ttu-id="887bb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="887bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="887bb-119">-Location</span><span class="sxs-lookup"><span data-stu-id="887bb-119">-Location</span></span>
<span data-ttu-id="887bb-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="887bb-120">The location of the resource</span></span>

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

### <span data-ttu-id="887bb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="887bb-121">-Name</span></span>
<span data-ttu-id="887bb-122">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="887bb-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="887bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="887bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="887bb-124">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="887bb-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="887bb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="887bb-125">-Tag</span></span>
<span data-ttu-id="887bb-126">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="887bb-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="887bb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="887bb-127">-Confirm</span></span>
<span data-ttu-id="887bb-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="887bb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887bb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887bb-129">-WhatIf</span></span>
<span data-ttu-id="887bb-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="887bb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="887bb-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="887bb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="887bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887bb-132">CommonParameters</span></span>
<span data-ttu-id="887bb-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887bb-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="887bb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887bb-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="887bb-135">INPUTS</span></span>

### <span data-ttu-id="887bb-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="887bb-136">None</span></span>

## <span data-ttu-id="887bb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="887bb-137">OUTPUTS</span></span>

### <span data-ttu-id="887bb-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="887bb-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="887bb-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="887bb-139">NOTES</span></span>

## <span data-ttu-id="887bb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="887bb-140">RELATED LINKS</span></span>
