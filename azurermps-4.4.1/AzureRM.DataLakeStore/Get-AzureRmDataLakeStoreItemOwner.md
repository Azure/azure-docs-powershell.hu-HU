---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679462"
---
# <span data-ttu-id="e0b11-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="e0b11-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="e0b11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0b11-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b11-103">Az adattó áruházban lévő fájl vagy mappa tulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b11-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0b11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0b11-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0b11-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0b11-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b11-106">A **Get-AzureRmDataLakeStoreItemOwner** parancsmag az Adattó áruházban lévő fájlok vagy mappák tulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b11-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e0b11-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0b11-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b11-108">Példa 1: a tulajdonos beszerzése egy címtárhoz</span><span class="sxs-lookup"><span data-stu-id="e0b11-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="e0b11-109">Ez a parancs megszerzi a felhasználó tulajdonosát az ContosoADL-fiók gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="e0b11-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="e0b11-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0b11-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b11-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e0b11-111">-Account</span></span>
<span data-ttu-id="e0b11-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b11-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e0b11-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e0b11-113">-Path</span></span>
<span data-ttu-id="e0b11-114">Az adattó-tároló elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="e0b11-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e0b11-115">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e0b11-115">-Type</span></span>
<span data-ttu-id="e0b11-116">Megadja, hogy milyen típusú tulajdonost kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="e0b11-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="e0b11-117">A paraméter elfogadható értékei a következők: felhasználó és csoport.</span><span class="sxs-lookup"><span data-stu-id="e0b11-117">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b11-118">-DefaultProfile</span></span>
<span data-ttu-id="e0b11-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0b11-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0b11-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b11-120">CommonParameters</span></span>
<span data-ttu-id="e0b11-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0b11-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b11-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b11-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b11-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b11-123">INPUTS</span></span>

## <span data-ttu-id="e0b11-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b11-124">OUTPUTS</span></span>

### <span data-ttu-id="e0b11-125">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e0b11-125">string</span></span>
<span data-ttu-id="e0b11-126">A megadott elem tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="e0b11-126">The owner of the specified item.</span></span>

## <span data-ttu-id="e0b11-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0b11-127">NOTES</span></span>

## <span data-ttu-id="e0b11-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0b11-128">RELATED LINKS</span></span>

[<span data-ttu-id="e0b11-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="e0b11-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


