---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4276b9477e51165e01c716095d5f4e2a4ea6ca69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494065"
---
# <span data-ttu-id="9e6df-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9e6df-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="9e6df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e6df-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6df-103">Az adattó áruházban lévő fájl vagy mappa tulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e6df-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e6df-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e6df-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6df-106">A **Get-AzureRmDataLakeStoreItemOwner** parancsmag az Adattó áruházban lévő fájlok vagy mappák tulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e6df-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9e6df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e6df-107">EXAMPLES</span></span>

### <span data-ttu-id="9e6df-108">Példa 1: a tulajdonos beszerzése egy címtárhoz</span><span class="sxs-lookup"><span data-stu-id="9e6df-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="9e6df-109">Ez a parancs megszerzi a felhasználó tulajdonosát az ContosoADL-fiók gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="9e6df-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="9e6df-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e6df-110">PARAMETERS</span></span>

### <span data-ttu-id="9e6df-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9e6df-111">-Account</span></span>
<span data-ttu-id="9e6df-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e6df-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9e6df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6df-113">-DefaultProfile</span></span>
<span data-ttu-id="9e6df-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e6df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e6df-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9e6df-115">-Path</span></span>
<span data-ttu-id="9e6df-116">Az adattó-tároló elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="9e6df-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9e6df-117">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="9e6df-117">-Type</span></span>
<span data-ttu-id="9e6df-118">Megadja, hogy milyen típusú tulajdonost kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="9e6df-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="9e6df-119">A paraméter elfogadható értékei a következők: felhasználó és csoport.</span><span class="sxs-lookup"><span data-stu-id="9e6df-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="9e6df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6df-120">CommonParameters</span></span>
<span data-ttu-id="9e6df-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e6df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6df-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6df-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6df-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e6df-123">INPUTS</span></span>

### <span data-ttu-id="9e6df-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9e6df-124">System.String</span></span>

### <span data-ttu-id="9e6df-125">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9e6df-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9e6df-126">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="9e6df-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="9e6df-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e6df-127">OUTPUTS</span></span>

### <span data-ttu-id="9e6df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9e6df-128">System.String</span></span>
<span data-ttu-id="9e6df-129">A megadott elem tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="9e6df-129">The owner of the specified item.</span></span>

## <span data-ttu-id="9e6df-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e6df-130">NOTES</span></span>

## <span data-ttu-id="9e6df-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e6df-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e6df-132">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9e6df-132">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


