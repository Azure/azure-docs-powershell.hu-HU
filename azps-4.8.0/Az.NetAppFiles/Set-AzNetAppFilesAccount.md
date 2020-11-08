---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024667"
---
# <span data-ttu-id="c83a2-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c83a2-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c83a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c83a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c83a2-103">Az Azure NetApp-fájlok (ANF) fiókját frissíti az új adatkészlettel.</span><span class="sxs-lookup"><span data-stu-id="c83a2-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="c83a2-104">Hasznos a kapcsolódó Active könyvtárak törléséhez.</span><span class="sxs-lookup"><span data-stu-id="c83a2-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="c83a2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c83a2-105">SYNTAX</span></span>

### <span data-ttu-id="c83a2-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c83a2-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83a2-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c83a2-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c83a2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c83a2-108">DESCRIPTION</span></span>
<span data-ttu-id="c83a2-109">A **set-AzNetAppFilesAccount** PARANCSMAG a ANF-fiókot módosítja.</span><span class="sxs-lookup"><span data-stu-id="c83a2-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="c83a2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c83a2-110">EXAMPLES</span></span>

### <span data-ttu-id="c83a2-111">Példa 1: ANF-fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="c83a2-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="c83a2-112">Ez a parancs egy frissítést hajt végre az adott fiókban.</span><span class="sxs-lookup"><span data-stu-id="c83a2-112">This command performs an update on the given account.</span></span> <span data-ttu-id="c83a2-113">Az Active Directory hiánya azt jelenti, hogy az törlődik a fiókból.</span><span class="sxs-lookup"><span data-stu-id="c83a2-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="c83a2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c83a2-114">PARAMETERS</span></span>

### <span data-ttu-id="c83a2-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c83a2-115">-ActiveDirectory</span></span>
<span data-ttu-id="c83a2-116">Az aktív könyvtárakat reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="c83a2-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="c83a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c83a2-117">-DefaultProfile</span></span>
<span data-ttu-id="c83a2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c83a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c83a2-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="c83a2-119">-Location</span></span>
<span data-ttu-id="c83a2-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="c83a2-120">The location of the resource</span></span>

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

### <span data-ttu-id="c83a2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c83a2-121">-Name</span></span>
<span data-ttu-id="c83a2-122">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="c83a2-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="c83a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c83a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="c83a2-124">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="c83a2-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c83a2-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="c83a2-125">-Tag</span></span>
<span data-ttu-id="c83a2-126">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="c83a2-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c83a2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c83a2-127">-Confirm</span></span>
<span data-ttu-id="c83a2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c83a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c83a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c83a2-129">-WhatIf</span></span>
<span data-ttu-id="c83a2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c83a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c83a2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c83a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c83a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c83a2-132">CommonParameters</span></span>
<span data-ttu-id="c83a2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c83a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c83a2-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c83a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c83a2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c83a2-135">INPUTS</span></span>

### <span data-ttu-id="c83a2-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="c83a2-136">None</span></span>

## <span data-ttu-id="c83a2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c83a2-137">OUTPUTS</span></span>

### <span data-ttu-id="c83a2-138">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c83a2-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c83a2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c83a2-139">NOTES</span></span>

## <span data-ttu-id="c83a2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c83a2-140">RELATED LINKS</span></span>
