---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499868"
---
# <span data-ttu-id="8ec58-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="8ec58-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="8ec58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ec58-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec58-103">Módosította az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét.</span><span class="sxs-lookup"><span data-stu-id="8ec58-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ec58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ec58-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ec58-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec58-106">A **set-AzureRmDataLakeStoreItemPermission** parancsmag módosította az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét.</span><span class="sxs-lookup"><span data-stu-id="8ec58-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8ec58-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8ec58-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec58-108">1. példa: az adott elemhez tartozó engedély oktális beállítása</span><span class="sxs-lookup"><span data-stu-id="8ec58-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="8ec58-109">Ez a parancs beállítja a fájlok 0770-ra való engedélyezését, ami a Sticky bit törlésére, a fájl tulajdonosának olvasási/írási/végrehajtási engedélyeinek beállítására, a fájl tulajdonosi csoportjának olvasási/írási/végrehajtási engedélyeinek beállítására, valamint az olvasás/írás/végrehajtás engedélyeinek törlésére vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="8ec58-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="8ec58-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ec58-110">PARAMETERS</span></span>

### <span data-ttu-id="8ec58-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8ec58-111">-Account</span></span>
<span data-ttu-id="8ec58-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec58-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec58-113">-DefaultProfile</span></span>
<span data-ttu-id="8ec58-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ec58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec58-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8ec58-115">-Path</span></span>
<span data-ttu-id="8ec58-116">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="8ec58-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec58-117">– Engedély</span><span class="sxs-lookup"><span data-stu-id="8ec58-117">-Permission</span></span>
<span data-ttu-id="8ec58-118">A fájlhoz vagy mappához az oktális formátumban megadott engedélyek (például "777")</span><span class="sxs-lookup"><span data-stu-id="8ec58-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec58-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ec58-119">-Confirm</span></span>
<span data-ttu-id="8ec58-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ec58-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec58-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec58-121">-WhatIf</span></span>
<span data-ttu-id="8ec58-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ec58-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec58-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ec58-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec58-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec58-124">CommonParameters</span></span>
<span data-ttu-id="8ec58-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ec58-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec58-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec58-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec58-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec58-127">INPUTS</span></span>

### <span data-ttu-id="8ec58-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="8ec58-128">None</span></span>
<span data-ttu-id="8ec58-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8ec58-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ec58-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec58-130">OUTPUTS</span></span>

### <span data-ttu-id="8ec58-131">bool</span><span class="sxs-lookup"><span data-stu-id="8ec58-131">bool</span></span>
<span data-ttu-id="8ec58-132">Az engedély sikeres frissítését követően igaz értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="8ec58-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="8ec58-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ec58-133">NOTES</span></span>
* <span data-ttu-id="8ec58-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="8ec58-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="8ec58-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ec58-135">RELATED LINKS</span></span>

[<span data-ttu-id="8ec58-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="8ec58-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


