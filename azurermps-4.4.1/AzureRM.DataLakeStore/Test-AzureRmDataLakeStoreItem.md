---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a5087c3c2d2354eb33ab9777687d43f56f3eb42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500060"
---
# <span data-ttu-id="101dc-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="101dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="101dc-102">SYNOPSIS</span></span>
<span data-ttu-id="101dc-103">Teszteli az adattó-tárolóban lévő fájlok vagy mappák létezését.</span><span class="sxs-lookup"><span data-stu-id="101dc-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="101dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="101dc-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="101dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="101dc-105">DESCRIPTION</span></span>
<span data-ttu-id="101dc-106">A **AzureRmDataLakeStoreItem** parancsmag teszteli az adattó-tárolóban lévő fájlok vagy mappák létezését.</span><span class="sxs-lookup"><span data-stu-id="101dc-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="101dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="101dc-107">EXAMPLES</span></span>

### <span data-ttu-id="101dc-108">Példa 1: fájl tesztelése</span><span class="sxs-lookup"><span data-stu-id="101dc-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="101dc-109">Ez a parancs azt vizsgálja, hogy a fájl Test.csv megtalálható-e a ContosoADL-fiókban.</span><span class="sxs-lookup"><span data-stu-id="101dc-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="101dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="101dc-110">PARAMETERS</span></span>

### <span data-ttu-id="101dc-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="101dc-111">-Account</span></span>
<span data-ttu-id="101dc-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="101dc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="101dc-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="101dc-113">-Path</span></span>
<span data-ttu-id="101dc-114">A vizsgálandó elem Data Lake Store elérési útját adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="101dc-114">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="101dc-115">-PathType</span><span class="sxs-lookup"><span data-stu-id="101dc-115">-PathType</span></span>
<span data-ttu-id="101dc-116">A vizsgálandó elem típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="101dc-116">Specifies the type of item to test.</span></span>
<span data-ttu-id="101dc-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="101dc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="101dc-118">Bármely</span><span class="sxs-lookup"><span data-stu-id="101dc-118">Any</span></span> 
- <span data-ttu-id="101dc-119">Fájl</span><span class="sxs-lookup"><span data-stu-id="101dc-119">File</span></span> 
- <span data-ttu-id="101dc-120">Mappa</span><span class="sxs-lookup"><span data-stu-id="101dc-120">Folder</span></span>

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

### <span data-ttu-id="101dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="101dc-121">-DefaultProfile</span></span>
<span data-ttu-id="101dc-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="101dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101dc-123">CommonParameters</span></span>
<span data-ttu-id="101dc-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="101dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101dc-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="101dc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101dc-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="101dc-126">INPUTS</span></span>

## <span data-ttu-id="101dc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="101dc-127">OUTPUTS</span></span>

### <span data-ttu-id="101dc-128">bool</span><span class="sxs-lookup"><span data-stu-id="101dc-128">bool</span></span>
<span data-ttu-id="101dc-129">True vagy FALSE: a megadott fájl vagy mappa létezését jelzi.</span><span class="sxs-lookup"><span data-stu-id="101dc-129">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="101dc-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="101dc-130">NOTES</span></span>

## <span data-ttu-id="101dc-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="101dc-131">RELATED LINKS</span></span>

[<span data-ttu-id="101dc-132">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-132">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="101dc-133">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-133">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="101dc-134">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-134">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="101dc-135">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-135">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="101dc-136">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-136">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="101dc-137">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="101dc-137">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


