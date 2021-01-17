---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465829"
---
# <span data-ttu-id="69d00-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="69d00-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="69d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69d00-102">SYNOPSIS</span></span>
<span data-ttu-id="69d00-103">A Data Lake Store-ban található fájl vagy mappa tulajdonosának lekérte.</span><span class="sxs-lookup"><span data-stu-id="69d00-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="69d00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69d00-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69d00-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69d00-105">DESCRIPTION</span></span>
<span data-ttu-id="69d00-106">A **Get-AzDataLakeStoreItemOwner** parancsmag lekérte egy fájl vagy mappa tulajdonosát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="69d00-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="69d00-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69d00-107">EXAMPLES</span></span>

### <span data-ttu-id="69d00-108">1. példa: Címtár tulajdonosának lekérte</span><span class="sxs-lookup"><span data-stu-id="69d00-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="69d00-109">Ez a parancs a ContosoADL-fiók gyökérkönyvtárának felhasználótulajdonosát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69d00-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="69d00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69d00-110">PARAMETERS</span></span>

### <span data-ttu-id="69d00-111">-Account</span><span class="sxs-lookup"><span data-stu-id="69d00-111">-Account</span></span>
<span data-ttu-id="69d00-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69d00-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="69d00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d00-113">-DefaultProfile</span></span>
<span data-ttu-id="69d00-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69d00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69d00-115">-Path</span><span class="sxs-lookup"><span data-stu-id="69d00-115">-Path</span></span>
<span data-ttu-id="69d00-116">Egy elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="69d00-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="69d00-117">-Type</span><span class="sxs-lookup"><span data-stu-id="69d00-117">-Type</span></span>
<span data-ttu-id="69d00-118">A lekért tulajdonos típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="69d00-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="69d00-119">A paraméter elfogadható értékei a következőek: Felhasználó és Csoport.</span><span class="sxs-lookup"><span data-stu-id="69d00-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="69d00-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d00-120">CommonParameters</span></span>
<span data-ttu-id="69d00-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d00-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d00-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d00-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d00-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69d00-123">INPUTS</span></span>

### <span data-ttu-id="69d00-124">System.String</span><span class="sxs-lookup"><span data-stu-id="69d00-124">System.String</span></span>

### <span data-ttu-id="69d00-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="69d00-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="69d00-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="69d00-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="69d00-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69d00-127">OUTPUTS</span></span>

### <span data-ttu-id="69d00-128">System.String</span><span class="sxs-lookup"><span data-stu-id="69d00-128">System.String</span></span>

## <span data-ttu-id="69d00-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69d00-129">NOTES</span></span>

## <span data-ttu-id="69d00-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69d00-130">RELATED LINKS</span></span>

[<span data-ttu-id="69d00-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="69d00-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


