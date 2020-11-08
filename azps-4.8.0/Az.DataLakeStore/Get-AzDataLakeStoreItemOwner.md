---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183064"
---
# <span data-ttu-id="19dd6-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="19dd6-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="19dd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="19dd6-103">Az adattó áruházban lévő fájl vagy mappa tulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19dd6-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="19dd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19dd6-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19dd6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="19dd6-106">A **Get-AzDataLakeStoreItemOwner** parancsmag az Adattó áruházban lévő fájlok vagy mappák tulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19dd6-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="19dd6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19dd6-107">EXAMPLES</span></span>

### <span data-ttu-id="19dd6-108">Példa 1: a tulajdonos beszerzése egy címtárhoz</span><span class="sxs-lookup"><span data-stu-id="19dd6-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="19dd6-109">Ez a parancs megszerzi a felhasználó tulajdonosát az ContosoADL-fiók gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="19dd6-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="19dd6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19dd6-110">PARAMETERS</span></span>

### <span data-ttu-id="19dd6-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="19dd6-111">-Account</span></span>
<span data-ttu-id="19dd6-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19dd6-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="19dd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dd6-113">-DefaultProfile</span></span>
<span data-ttu-id="19dd6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19dd6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19dd6-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="19dd6-115">-Path</span></span>
<span data-ttu-id="19dd6-116">Az adattó-tároló elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="19dd6-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="19dd6-117">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="19dd6-117">-Type</span></span>
<span data-ttu-id="19dd6-118">Megadja, hogy milyen típusú tulajdonost kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="19dd6-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="19dd6-119">A paraméter elfogadható értékei a következők: felhasználó és csoport.</span><span class="sxs-lookup"><span data-stu-id="19dd6-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="19dd6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dd6-120">CommonParameters</span></span>
<span data-ttu-id="19dd6-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19dd6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dd6-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19dd6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dd6-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19dd6-123">INPUTS</span></span>

### <span data-ttu-id="19dd6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="19dd6-124">System.String</span></span>

### <span data-ttu-id="19dd6-125">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="19dd6-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="19dd6-126">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="19dd6-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="19dd6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19dd6-127">OUTPUTS</span></span>

### <span data-ttu-id="19dd6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="19dd6-128">System.String</span></span>

## <span data-ttu-id="19dd6-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19dd6-129">NOTES</span></span>

## <span data-ttu-id="19dd6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19dd6-130">RELATED LINKS</span></span>

[<span data-ttu-id="19dd6-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="19dd6-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


