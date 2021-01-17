---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465802"
---
# <span data-ttu-id="3bbbe-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="3bbbe-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="3bbbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbbe-103">Törölt fájl vagy mappa visszaállítása az Azure Data Lake szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="3bbbe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bbbe-104">SYNTAX</span></span>

### <span data-ttu-id="3bbbe-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bbbe-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bbbe-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3bbbe-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bbbe-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bbbe-107">DESCRIPTION</span></span>
<span data-ttu-id="3bbbe-108">A **Restore-AzDataLakeStoreDeletedItem** parancsmag visszaállít egy törölt fájlt vagy mappát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="3bbbe-109">A Get-AzDataLakeStoreDeletedItem által visszaadott törölt elem elérési útját igényli a kukában.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="3bbbe-110">Figyelem: A fájlok törlése a legjobb munkamennyiség-művelet.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="3bbbe-111">Nincs garancia arra, hogy a fájlok a törlés után visszaállíthatóak.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="3bbbe-112">Az API használata az engedélyezési listán keresztül engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="3bbbe-113">Ha az ADL-fiókja nincs whitelisted listán, akkor az api használata kivételt képez a Nem megvalósított kivételtől.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="3bbbe-114">További információért és segítségért forduljon a Microsoft ügyfélszolgálatához.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="3bbbe-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bbbe-115">EXAMPLES</span></span>

### <span data-ttu-id="3bbbe-116">1. példa: Fájl visszaállítása a Data Lake Store-ból a -force beállítással</span><span class="sxs-lookup"><span data-stu-id="3bbbe-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="3bbbe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bbbe-117">PARAMETERS</span></span>

### <span data-ttu-id="3bbbe-118">-Account</span><span class="sxs-lookup"><span data-stu-id="3bbbe-118">-Account</span></span>
<span data-ttu-id="3bbbe-119">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3bbbe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbbe-120">-DefaultProfile</span></span>
<span data-ttu-id="3bbbe-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbbe-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="3bbbe-122">-DeletedItem</span></span>
<span data-ttu-id="3bbbe-123">A törölt elem objektum.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-123">The deleted item object.</span></span>

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

### <span data-ttu-id="3bbbe-124">-Destination</span><span class="sxs-lookup"><span data-stu-id="3bbbe-124">-Destination</span></span>
<span data-ttu-id="3bbbe-125">A törölt fájl vagy mappa visszaállításának cél elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="3bbbe-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3bbbe-126">-Force</span></span>
<span data-ttu-id="3bbbe-127">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3bbbe-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bbbe-128">-PassThru</span></span>
<span data-ttu-id="3bbbe-129">A sikeres visszatérési logikai érték igaz.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="3bbbe-130">-Path</span><span class="sxs-lookup"><span data-stu-id="3bbbe-130">-Path</span></span>
<span data-ttu-id="3bbbe-131">A törölt fájl vagy mappa elérési útja a kukában.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="3bbbe-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="3bbbe-132">-RestoreAction</span></span>
<span data-ttu-id="3bbbe-133">Célnévütközések "másolása" vagy "felülírása" művelet</span><span class="sxs-lookup"><span data-stu-id="3bbbe-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="3bbbe-134">-Type</span><span class="sxs-lookup"><span data-stu-id="3bbbe-134">-Type</span></span>
<span data-ttu-id="3bbbe-135">A visszaállított bejegyzés típusa – "fájl" vagy "mappa"</span><span class="sxs-lookup"><span data-stu-id="3bbbe-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="3bbbe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbbe-136">CommonParameters</span></span>
<span data-ttu-id="3bbbe-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bbbe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbbe-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbbe-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbbe-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bbbe-139">INPUTS</span></span>

### <span data-ttu-id="3bbbe-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3bbbe-140">System.String</span></span>

## <span data-ttu-id="3bbbe-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bbbe-141">OUTPUTS</span></span>

### <span data-ttu-id="3bbbe-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="3bbbe-142">None</span></span>

## <span data-ttu-id="3bbbe-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bbbe-143">NOTES</span></span>

## <span data-ttu-id="3bbbe-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bbbe-144">RELATED LINKS</span></span>

[<span data-ttu-id="3bbbe-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="3bbbe-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)