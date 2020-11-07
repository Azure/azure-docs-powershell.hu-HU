---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: e6fa7a00218e52eae6b0323bc5e8ac25459986ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845026"
---
# <span data-ttu-id="a5fba-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a5fba-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a5fba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5fba-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fba-103">Az Azure NetApp-fájlok (ANF) fiókját frissíti a megadható választható módosítóval összhangban.</span><span class="sxs-lookup"><span data-stu-id="a5fba-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="a5fba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5fba-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="a5fba-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fba-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5fba-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fba-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fba-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fba-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5fba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5fba-108">DESCRIPTION</span></span>
<span data-ttu-id="a5fba-109">Az **Update-AzNetAppFilesAccount** parancsmag módosította az ANF-fiókját.</span><span class="sxs-lookup"><span data-stu-id="a5fba-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="a5fba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5fba-110">EXAMPLES</span></span>

### <span data-ttu-id="a5fba-111">Példa 1: ANF-fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="a5fba-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="a5fba-112">Ez a parancs egy olyan frissítést hajt végre az adott fiókon, amelynek a címkéit a megadott értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="a5fba-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="a5fba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5fba-113">PARAMETERS</span></span>

### <span data-ttu-id="a5fba-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="a5fba-114">-ActiveDirectories</span></span>
<span data-ttu-id="a5fba-115">Az aktív könyvtárakat reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="a5fba-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fba-116">-DefaultProfile</span></span>
<span data-ttu-id="a5fba-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5fba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5fba-118">-InputObject</span></span>
<span data-ttu-id="a5fba-119">A módosítani kívánt ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="a5fba-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5fba-120">-Location</span></span>
<span data-ttu-id="a5fba-121">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="a5fba-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5fba-122">-Name</span></span>
<span data-ttu-id="a5fba-123">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="a5fba-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5fba-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5fba-125">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="a5fba-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5fba-126">-ResourceId</span></span>
<span data-ttu-id="a5fba-127">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a5fba-127">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="a5fba-128">-Tag</span></span>
<span data-ttu-id="a5fba-129">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="a5fba-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5fba-130">-Confirm</span></span>
<span data-ttu-id="a5fba-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5fba-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fba-132">-WhatIf</span></span>
<span data-ttu-id="a5fba-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5fba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5fba-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5fba-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fba-135">CommonParameters</span></span>
<span data-ttu-id="a5fba-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5fba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a5fba-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5fba-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fba-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5fba-138">INPUTS</span></span>

### <span data-ttu-id="a5fba-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5fba-139">None</span></span>

## <span data-ttu-id="a5fba-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5fba-140">OUTPUTS</span></span>

### <span data-ttu-id="a5fba-141">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a5fba-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a5fba-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5fba-142">NOTES</span></span>

## <span data-ttu-id="a5fba-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5fba-143">RELATED LINKS</span></span>
