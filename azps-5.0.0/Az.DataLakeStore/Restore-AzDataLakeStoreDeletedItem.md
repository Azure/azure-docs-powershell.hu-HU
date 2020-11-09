---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297764"
---
# <span data-ttu-id="731a9-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="731a9-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="731a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="731a9-102">SYNOPSIS</span></span>
<span data-ttu-id="731a9-103">A törölt fájlok vagy mappák visszaállítása az Azure Data Lakeben.</span><span class="sxs-lookup"><span data-stu-id="731a9-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="731a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="731a9-104">SYNTAX</span></span>

### <span data-ttu-id="731a9-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="731a9-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="731a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="731a9-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="731a9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="731a9-107">DESCRIPTION</span></span>
<span data-ttu-id="731a9-108">A **Restore-AzDataLakeStoreDeletedItem** parancsmag visszaállítja a törölt fájlokat vagy mappákat az Adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="731a9-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="731a9-109">A AzDataLakeStoreDeletedItem a törölt elemek elérési útját igényli a kukában.</span><span class="sxs-lookup"><span data-stu-id="731a9-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="731a9-110">Figyelmeztetés: a törlés visszavonása ajánlott művelet.</span><span class="sxs-lookup"><span data-stu-id="731a9-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="731a9-111">Nincs garancia arra, hogy a fájl törlés után visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="731a9-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="731a9-112">Az API használatát a whitelisten keresztül engedélyezheti.</span><span class="sxs-lookup"><span data-stu-id="731a9-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="731a9-113">Ha az ADL-fiókja nem whitelist, akkor ezzel az API-val nem fog bevezetni a kivételt.</span><span class="sxs-lookup"><span data-stu-id="731a9-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="731a9-114">További információért és segítségért forduljon a Microsoft ügyfélszolgálatához.</span><span class="sxs-lookup"><span data-stu-id="731a9-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="731a9-115">Példák</span><span class="sxs-lookup"><span data-stu-id="731a9-115">EXAMPLES</span></span>

### <span data-ttu-id="731a9-116">1. példa: fájl visszaállítása az adattó áruházból a-Force beállítás használatával</span><span class="sxs-lookup"><span data-stu-id="731a9-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="731a9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="731a9-117">PARAMETERS</span></span>

### <span data-ttu-id="731a9-118">-Fiók</span><span class="sxs-lookup"><span data-stu-id="731a9-118">-Account</span></span>
<span data-ttu-id="731a9-119">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="731a9-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="731a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731a9-120">-DefaultProfile</span></span>
<span data-ttu-id="731a9-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="731a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="731a9-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="731a9-122">-DeletedItem</span></span>
<span data-ttu-id="731a9-123">A törölt elem objektum.</span><span class="sxs-lookup"><span data-stu-id="731a9-123">The deleted item object.</span></span>

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

### <span data-ttu-id="731a9-124">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="731a9-124">-Destination</span></span>
<span data-ttu-id="731a9-125">A hely elérési útja, ahová a törölt fájlt vagy mappát vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="731a9-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="731a9-126">-Force</span><span class="sxs-lookup"><span data-stu-id="731a9-126">-Force</span></span>
<span data-ttu-id="731a9-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="731a9-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="731a9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="731a9-128">-PassThru</span></span>
<span data-ttu-id="731a9-129">IGAZ logikai érték visszaadása a siker érdekében.</span><span class="sxs-lookup"><span data-stu-id="731a9-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="731a9-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="731a9-130">-Path</span></span>
<span data-ttu-id="731a9-131">A törölt fájl vagy mappa elérési útvonala a kukában.</span><span class="sxs-lookup"><span data-stu-id="731a9-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="731a9-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="731a9-132">-RestoreAction</span></span>
<span data-ttu-id="731a9-133">A rendeltetési hely nevének ütközése – "másolat" vagy "felülírás"</span><span class="sxs-lookup"><span data-stu-id="731a9-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="731a9-134">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="731a9-134">-Type</span></span>
<span data-ttu-id="731a9-135">A visszaállítandó bejegyzés típusa – "fájl" vagy "mappa"</span><span class="sxs-lookup"><span data-stu-id="731a9-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="731a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731a9-136">CommonParameters</span></span>
<span data-ttu-id="731a9-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="731a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731a9-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731a9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731a9-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="731a9-139">INPUTS</span></span>

### <span data-ttu-id="731a9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="731a9-140">System.String</span></span>

## <span data-ttu-id="731a9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="731a9-141">OUTPUTS</span></span>

### <span data-ttu-id="731a9-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="731a9-142">None</span></span>

## <span data-ttu-id="731a9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="731a9-143">NOTES</span></span>

## <span data-ttu-id="731a9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="731a9-144">RELATED LINKS</span></span>

[<span data-ttu-id="731a9-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="731a9-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)