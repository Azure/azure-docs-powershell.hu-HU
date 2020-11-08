---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 621d4d29d061566e894617d5e918440ba531a041
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185714"
---
# <span data-ttu-id="c3f99-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c3f99-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c3f99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3f99-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f99-103">Az Azure NetApp-fájlok (ANF) fiókját frissíti a megadható választható módosítóval összhangban.</span><span class="sxs-lookup"><span data-stu-id="c3f99-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c3f99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3f99-104">SYNTAX</span></span>

### <span data-ttu-id="c3f99-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3f99-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f99-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3f99-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f99-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3f99-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f99-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3f99-108">DESCRIPTION</span></span>
<span data-ttu-id="c3f99-109">Az **Update-AzNetAppFilesAccount** parancsmag módosította az ANF-fiókját.</span><span class="sxs-lookup"><span data-stu-id="c3f99-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="c3f99-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3f99-110">EXAMPLES</span></span>

### <span data-ttu-id="c3f99-111">Példa 1: ANF-fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="c3f99-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="c3f99-112">Ez a parancs egy olyan frissítést hajt végre az adott fiókon, amelynek a címkéit a megadott értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="c3f99-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="c3f99-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3f99-113">PARAMETERS</span></span>

### <span data-ttu-id="c3f99-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c3f99-114">-ActiveDirectory</span></span>
<span data-ttu-id="c3f99-115">Az aktív könyvtárakat reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="c3f99-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="c3f99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f99-116">-DefaultProfile</span></span>
<span data-ttu-id="c3f99-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3f99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3f99-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3f99-118">-InputObject</span></span>
<span data-ttu-id="c3f99-119">A módosítani kívánt ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="c3f99-119">The account object to update</span></span>

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

### <span data-ttu-id="c3f99-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="c3f99-120">-Location</span></span>
<span data-ttu-id="c3f99-121">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="c3f99-121">The location of the resource</span></span>

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

### <span data-ttu-id="c3f99-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3f99-122">-Name</span></span>
<span data-ttu-id="c3f99-123">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="c3f99-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="c3f99-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3f99-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3f99-125">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="c3f99-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c3f99-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3f99-126">-ResourceId</span></span>
<span data-ttu-id="c3f99-127">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c3f99-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="c3f99-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="c3f99-128">-Tag</span></span>
<span data-ttu-id="c3f99-129">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="c3f99-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c3f99-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3f99-130">-Confirm</span></span>
<span data-ttu-id="c3f99-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3f99-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f99-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f99-132">-WhatIf</span></span>
<span data-ttu-id="c3f99-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3f99-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f99-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3f99-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f99-135">CommonParameters</span></span>
<span data-ttu-id="c3f99-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3f99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f99-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3f99-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f99-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3f99-138">INPUTS</span></span>

### <span data-ttu-id="c3f99-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="c3f99-139">None</span></span>

## <span data-ttu-id="c3f99-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3f99-140">OUTPUTS</span></span>

### <span data-ttu-id="c3f99-141">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c3f99-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c3f99-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3f99-142">NOTES</span></span>

## <span data-ttu-id="c3f99-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3f99-143">RELATED LINKS</span></span>
