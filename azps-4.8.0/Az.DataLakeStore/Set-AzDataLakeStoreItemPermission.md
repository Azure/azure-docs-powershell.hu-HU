---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182314"
---
# <span data-ttu-id="669d1-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="669d1-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="669d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="669d1-102">SYNOPSIS</span></span>
<span data-ttu-id="669d1-103">Módosította az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét.</span><span class="sxs-lookup"><span data-stu-id="669d1-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="669d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="669d1-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="669d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="669d1-105">DESCRIPTION</span></span>
<span data-ttu-id="669d1-106">A **set-AzDataLakeStoreItemPermission** parancsmag módosította az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét.</span><span class="sxs-lookup"><span data-stu-id="669d1-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="669d1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="669d1-107">EXAMPLES</span></span>

### <span data-ttu-id="669d1-108">1. példa: az adott elemhez tartozó engedély oktális beállítása</span><span class="sxs-lookup"><span data-stu-id="669d1-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="669d1-109">Ez a parancs beállítja a fájlok 0770-ra való engedélyezését, ami a Sticky bit törlésére, a fájl tulajdonosának olvasási/írási/végrehajtási engedélyeinek beállítására, a fájl tulajdonosi csoportjának olvasási/írási/végrehajtási engedélyeinek beállítására, valamint az olvasás/írás/végrehajtás engedélyeinek törlésére vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="669d1-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="669d1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="669d1-110">PARAMETERS</span></span>

### <span data-ttu-id="669d1-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="669d1-111">-Account</span></span>
<span data-ttu-id="669d1-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="669d1-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="669d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669d1-113">-DefaultProfile</span></span>
<span data-ttu-id="669d1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="669d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="669d1-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="669d1-115">-Path</span></span>
<span data-ttu-id="669d1-116">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="669d1-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="669d1-117">– Engedély</span><span class="sxs-lookup"><span data-stu-id="669d1-117">-Permission</span></span>
<span data-ttu-id="669d1-118">A fájlhoz vagy mappához az oktális formátumban megadott engedélyek (például "777")</span><span class="sxs-lookup"><span data-stu-id="669d1-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="669d1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="669d1-119">-Confirm</span></span>
<span data-ttu-id="669d1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="669d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669d1-121">-WhatIf</span></span>
<span data-ttu-id="669d1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="669d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="669d1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="669d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="669d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669d1-124">CommonParameters</span></span>
<span data-ttu-id="669d1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="669d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669d1-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="669d1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669d1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="669d1-127">INPUTS</span></span>

### <span data-ttu-id="669d1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="669d1-128">System.String</span></span>

### <span data-ttu-id="669d1-129">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="669d1-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="669d1-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="669d1-130">System.Int32</span></span>

## <span data-ttu-id="669d1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="669d1-131">OUTPUTS</span></span>

### <span data-ttu-id="669d1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="669d1-132">System.Boolean</span></span>

## <span data-ttu-id="669d1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="669d1-133">NOTES</span></span>
* <span data-ttu-id="669d1-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="669d1-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="669d1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="669d1-135">RELATED LINKS</span></span>

[<span data-ttu-id="669d1-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="669d1-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


