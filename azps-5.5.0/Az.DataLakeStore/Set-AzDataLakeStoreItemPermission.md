---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153379"
---
# <span data-ttu-id="4b6ac-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4b6ac-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="4b6ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6ac-103">Módosítja a Data Lake Store-ban tárolt fájlok vagy mappák engedély oktális engedélyét.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4b6ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b6ac-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b6ac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b6ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4b6ac-106">A **Set-AzDataLakeStoreItemPermission** parancsmag módosítja a Data Lake Store-ban található fájlok vagy mappák engedélyeinek oktális engedélyét.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4b6ac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b6ac-107">EXAMPLES</span></span>

### <span data-ttu-id="4b6ac-108">1. példa: Elem engedélyeinek oktális beállítása</span><span class="sxs-lookup"><span data-stu-id="4b6ac-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="4b6ac-109">Ez a parancs a fájl oktális engedélyét 0770-re állítja, azaz törli a berakott bitet, olvasási/írási/végrehajtási engedélyeket állít be a fájl tulajdonosának, olvasási/írási/végrehajtási engedélyeket állít be a fájl tulajdonosa csoportjához, valamint törli az olvasási/írási/végrehajtási engedélyeket más fájlokhoz.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="4b6ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b6ac-110">PARAMETERS</span></span>

### <span data-ttu-id="4b6ac-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4b6ac-111">-Account</span></span>
<span data-ttu-id="4b6ac-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6ac-113">-DefaultProfile</span></span>
<span data-ttu-id="4b6ac-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b6ac-115">-Path</span><span class="sxs-lookup"><span data-stu-id="4b6ac-115">-Path</span></span>
<span data-ttu-id="4b6ac-116">A fájl vagy mappa Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="4b6ac-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ac-117">-Permission</span><span class="sxs-lookup"><span data-stu-id="4b6ac-117">-Permission</span></span>
<span data-ttu-id="4b6ac-118">A fájlra vagy mappára vonatkozó, oktálisan (például "777") kifejezett engedélyek</span><span class="sxs-lookup"><span data-stu-id="4b6ac-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ac-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b6ac-119">-Confirm</span></span>
<span data-ttu-id="4b6ac-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6ac-121">-WhatIf</span></span>
<span data-ttu-id="4b6ac-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b6ac-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6ac-124">CommonParameters</span></span>
<span data-ttu-id="4b6ac-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6ac-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6ac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6ac-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b6ac-127">INPUTS</span></span>

### <span data-ttu-id="4b6ac-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b6ac-128">System.String</span></span>

### <span data-ttu-id="4b6ac-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4b6ac-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4b6ac-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4b6ac-130">System.Int32</span></span>

## <span data-ttu-id="4b6ac-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b6ac-131">OUTPUTS</span></span>

### <span data-ttu-id="4b6ac-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b6ac-132">System.Boolean</span></span>

## <span data-ttu-id="4b6ac-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b6ac-133">NOTES</span></span>
* <span data-ttu-id="4b6ac-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4b6ac-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="4b6ac-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b6ac-135">RELATED LINKS</span></span>

[<span data-ttu-id="4b6ac-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4b6ac-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


