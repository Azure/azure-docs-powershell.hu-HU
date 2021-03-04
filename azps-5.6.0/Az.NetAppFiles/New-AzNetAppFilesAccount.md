---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 588952f9f3aa0cb9c7351ee862ad6db82d66f85d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926865"
---
# <span data-ttu-id="5b4f0-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5b4f0-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="5b4f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4f0-103">Létrehoz egy új Azure NetApp-fájlokat (ANF-fiókot).</span><span class="sxs-lookup"><span data-stu-id="5b4f0-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="5b4f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b4f0-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b4f0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="5b4f0-106">A **New-AzNetAppFilesAccount** parancsmag ANF-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5b4f0-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="5b4f0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b4f0-107">EXAMPLES</span></span>

### <span data-ttu-id="5b4f0-108">1. példa: ANF-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="5b4f0-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="5b4f0-109">Ez a parancs létrehozza az új ANF-fiókot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="5b4f0-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="5b4f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b4f0-110">PARAMETERS</span></span>

### <span data-ttu-id="5b4f0-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5b4f0-111">-ActiveDirectory</span></span>
<span data-ttu-id="5b4f0-112">Az aktív könyvtárakat képviselő kivonatos tömb</span><span class="sxs-lookup"><span data-stu-id="5b4f0-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="5b4f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4f0-113">-DefaultProfile</span></span>
<span data-ttu-id="5b4f0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b4f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4f0-115">-Location</span><span class="sxs-lookup"><span data-stu-id="5b4f0-115">-Location</span></span>
<span data-ttu-id="5b4f0-116">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="5b4f0-116">The location of the resource</span></span>

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

### <span data-ttu-id="5b4f0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5b4f0-117">-Name</span></span>
<span data-ttu-id="5b4f0-118">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="5b4f0-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="5b4f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="5b4f0-120">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="5b4f0-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5b4f0-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b4f0-121">-Tag</span></span>
<span data-ttu-id="5b4f0-122">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="5b4f0-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="5b4f0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b4f0-123">-Confirm</span></span>
<span data-ttu-id="5b4f0-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b4f0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4f0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4f0-125">-WhatIf</span></span>
<span data-ttu-id="5b4f0-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b4f0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4f0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b4f0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4f0-128">CommonParameters</span></span>
<span data-ttu-id="5b4f0-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4f0-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b4f0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4f0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b4f0-131">INPUTS</span></span>

### <span data-ttu-id="5b4f0-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="5b4f0-132">None</span></span>

## <span data-ttu-id="5b4f0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b4f0-133">OUTPUTS</span></span>

### <span data-ttu-id="5b4f0-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5b4f0-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5b4f0-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b4f0-135">NOTES</span></span>

## <span data-ttu-id="5b4f0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b4f0-136">RELATED LINKS</span></span>
