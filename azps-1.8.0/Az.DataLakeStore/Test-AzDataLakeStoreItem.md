---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671044"
---
# <span data-ttu-id="85368-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="85368-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85368-102">SYNOPSIS</span></span>
<span data-ttu-id="85368-103">Teszteli az adattó-tárolóban lévő fájlok vagy mappák létezését.</span><span class="sxs-lookup"><span data-stu-id="85368-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="85368-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85368-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85368-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85368-105">DESCRIPTION</span></span>
<span data-ttu-id="85368-106">A **AzDataLakeStoreItem** parancsmag teszteli az adattó-tárolóban lévő fájlok vagy mappák létezését.</span><span class="sxs-lookup"><span data-stu-id="85368-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="85368-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85368-107">EXAMPLES</span></span>

### <span data-ttu-id="85368-108">Példa 1: fájl tesztelése</span><span class="sxs-lookup"><span data-stu-id="85368-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="85368-109">Ez a parancs azt vizsgálja, hogy a fájl Test.csv megtalálható-e a ContosoADL-fiókban.</span><span class="sxs-lookup"><span data-stu-id="85368-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="85368-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85368-110">PARAMETERS</span></span>

### <span data-ttu-id="85368-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="85368-111">-Account</span></span>
<span data-ttu-id="85368-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85368-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="85368-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85368-113">-DefaultProfile</span></span>
<span data-ttu-id="85368-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85368-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85368-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="85368-115">-Path</span></span>
<span data-ttu-id="85368-116">A vizsgálandó elem Data Lake Store elérési útját adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="85368-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="85368-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="85368-117">-PathType</span></span>
<span data-ttu-id="85368-118">A vizsgálandó elem típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85368-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="85368-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="85368-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85368-120">Bármely</span><span class="sxs-lookup"><span data-stu-id="85368-120">Any</span></span> 
- <span data-ttu-id="85368-121">Fájl</span><span class="sxs-lookup"><span data-stu-id="85368-121">File</span></span> 
- <span data-ttu-id="85368-122">Mappa</span><span class="sxs-lookup"><span data-stu-id="85368-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85368-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85368-123">CommonParameters</span></span>
<span data-ttu-id="85368-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85368-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85368-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85368-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85368-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85368-126">INPUTS</span></span>

### <span data-ttu-id="85368-127">System. String</span><span class="sxs-lookup"><span data-stu-id="85368-127">System.String</span></span>

### <span data-ttu-id="85368-128">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="85368-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="85368-129">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="85368-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="85368-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85368-130">OUTPUTS</span></span>

### <span data-ttu-id="85368-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85368-131">System.Boolean</span></span>

## <span data-ttu-id="85368-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85368-132">NOTES</span></span>

## <span data-ttu-id="85368-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85368-133">RELATED LINKS</span></span>

[<span data-ttu-id="85368-134">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="85368-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="85368-136">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="85368-137">Bekapcsolódás a AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="85368-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="85368-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85368-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


