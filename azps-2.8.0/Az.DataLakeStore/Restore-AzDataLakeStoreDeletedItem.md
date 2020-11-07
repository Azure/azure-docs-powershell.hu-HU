---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666809"
---
# <span data-ttu-id="0126c-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0126c-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="0126c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0126c-102">SYNOPSIS</span></span>
<span data-ttu-id="0126c-103">A törölt fájlok vagy mappák visszaállítása az Azure Data Lakeben.</span><span class="sxs-lookup"><span data-stu-id="0126c-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="0126c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0126c-104">SYNTAX</span></span>

### <span data-ttu-id="0126c-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0126c-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0126c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0126c-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0126c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0126c-107">DESCRIPTION</span></span>
<span data-ttu-id="0126c-108">A **Restore-AzDataLakeStoreDeletedItem** parancsmag visszaállítja a törölt fájlokat vagy mappákat az Adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="0126c-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="0126c-109">A AzDataLakeStoreDeletedItem a törölt elemek elérési útját igényli a kukában.</span><span class="sxs-lookup"><span data-stu-id="0126c-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="0126c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0126c-110">EXAMPLES</span></span>

### <span data-ttu-id="0126c-111">1. példa: fájl visszaállítása az adattó áruházból a-Force beállítás használatával</span><span class="sxs-lookup"><span data-stu-id="0126c-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="0126c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0126c-112">PARAMETERS</span></span>

### <span data-ttu-id="0126c-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="0126c-113">-Account</span></span>
<span data-ttu-id="0126c-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0126c-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0126c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0126c-115">-DefaultProfile</span></span>
<span data-ttu-id="0126c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0126c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0126c-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="0126c-117">-DeletedItem</span></span>
<span data-ttu-id="0126c-118">A törölt elem objektum.</span><span class="sxs-lookup"><span data-stu-id="0126c-118">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-119">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="0126c-119">-Destination</span></span>
<span data-ttu-id="0126c-120">A hely elérési útja, ahová a törölt fájlt vagy mappát vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="0126c-120">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0126c-121">-Force</span></span>
<span data-ttu-id="0126c-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0126c-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0126c-123">-PassThru</span></span>
<span data-ttu-id="0126c-124">IGAZ logikai érték visszaadása a siker érdekében.</span><span class="sxs-lookup"><span data-stu-id="0126c-124">Return boolean true on success.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-125">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0126c-125">-Path</span></span>
<span data-ttu-id="0126c-126">A törölt fájl vagy mappa elérési útvonala a kukában.</span><span class="sxs-lookup"><span data-stu-id="0126c-126">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="0126c-127">-RestoreAction</span></span>
<span data-ttu-id="0126c-128">A rendeltetési hely nevének ütközése – "másolat" vagy "felülírás"</span><span class="sxs-lookup"><span data-stu-id="0126c-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-129">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="0126c-129">-Type</span></span>
<span data-ttu-id="0126c-130">A visszaállítandó bejegyzés típusa – "fájl" vagy "mappa"</span><span class="sxs-lookup"><span data-stu-id="0126c-130">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0126c-131">CommonParameters</span></span>
<span data-ttu-id="0126c-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0126c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0126c-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0126c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0126c-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0126c-134">INPUTS</span></span>

### <span data-ttu-id="0126c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0126c-135">System.String</span></span>

## <span data-ttu-id="0126c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0126c-136">OUTPUTS</span></span>

### <span data-ttu-id="0126c-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="0126c-137">None</span></span>

## <span data-ttu-id="0126c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0126c-138">NOTES</span></span>

## <span data-ttu-id="0126c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0126c-139">RELATED LINKS</span></span>

[<span data-ttu-id="0126c-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0126c-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)