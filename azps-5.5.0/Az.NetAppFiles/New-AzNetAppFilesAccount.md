---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152091"
---
# <span data-ttu-id="4ccb2-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4ccb2-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="4ccb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ccb2-102">SYNOPSIS</span></span>
<span data-ttu-id="4ccb2-103">Létrehoz egy új Azure NetApp-fájlokat (ANF-fiókot).</span><span class="sxs-lookup"><span data-stu-id="4ccb2-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="4ccb2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ccb2-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ccb2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ccb2-105">DESCRIPTION</span></span>
<span data-ttu-id="4ccb2-106">A **New-AzNetAppFilesAccount** parancsmag ANF-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4ccb2-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="4ccb2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ccb2-107">EXAMPLES</span></span>

### <span data-ttu-id="4ccb2-108">1. példa: ANF-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ccb2-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="4ccb2-109">Ez a parancs létrehozza az új ANF-fiókot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="4ccb2-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="4ccb2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ccb2-110">PARAMETERS</span></span>

### <span data-ttu-id="4ccb2-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4ccb2-111">-ActiveDirectory</span></span>
<span data-ttu-id="4ccb2-112">Az aktív könyvtárakat képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="4ccb2-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="4ccb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ccb2-113">-DefaultProfile</span></span>
<span data-ttu-id="4ccb2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ccb2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ccb2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4ccb2-115">-Location</span></span>
<span data-ttu-id="4ccb2-116">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="4ccb2-116">The location of the resource</span></span>

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

### <span data-ttu-id="4ccb2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4ccb2-117">-Name</span></span>
<span data-ttu-id="4ccb2-118">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="4ccb2-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="4ccb2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ccb2-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ccb2-120">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="4ccb2-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4ccb2-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ccb2-121">-Tag</span></span>
<span data-ttu-id="4ccb2-122">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="4ccb2-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="4ccb2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ccb2-123">-Confirm</span></span>
<span data-ttu-id="4ccb2-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ccb2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ccb2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ccb2-125">-WhatIf</span></span>
<span data-ttu-id="4ccb2-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ccb2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ccb2-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ccb2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ccb2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ccb2-128">CommonParameters</span></span>
<span data-ttu-id="4ccb2-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ccb2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ccb2-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ccb2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ccb2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ccb2-131">INPUTS</span></span>

### <span data-ttu-id="4ccb2-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ccb2-132">None</span></span>

## <span data-ttu-id="4ccb2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ccb2-133">OUTPUTS</span></span>

### <span data-ttu-id="4ccb2-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4ccb2-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4ccb2-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ccb2-135">NOTES</span></span>

## <span data-ttu-id="4ccb2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ccb2-136">RELATED LINKS</span></span>
