---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680891"
---
# <span data-ttu-id="3469e-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="3469e-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="3469e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3469e-102">SYNOPSIS</span></span>
<span data-ttu-id="3469e-103">Módosítja egy fájl vagy mappa tulajdonosát az adattó-áruházban.</span><span class="sxs-lookup"><span data-stu-id="3469e-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3469e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3469e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3469e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3469e-105">DESCRIPTION</span></span>
<span data-ttu-id="3469e-106">A **set-AzureRmDataLakeStoreItemOwner** parancsmag módosította az adattó-tárolóban lévő fájlok vagy mappák tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="3469e-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3469e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3469e-107">EXAMPLES</span></span>

### <span data-ttu-id="3469e-108">Példa 1: egy elem tulajdonosának beállítása</span><span class="sxs-lookup"><span data-stu-id="3469e-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="3469e-109">Ez a parancs beállítja a gyökérkönyvtár tulajdonosát az Patti Fuller-nek.</span><span class="sxs-lookup"><span data-stu-id="3469e-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="3469e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3469e-110">PARAMETERS</span></span>

### <span data-ttu-id="3469e-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="3469e-111">-Account</span></span>
<span data-ttu-id="3469e-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3469e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3469e-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3469e-113">-Id</span></span>
<span data-ttu-id="3469e-114">Itt adhatja meg a tulajdonosként használandó AzureActive-felhasználó,-csoport vagy-szolgáltató objektum-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="3469e-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3469e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3469e-115">-PassThru</span></span>
<span data-ttu-id="3469e-116">Jelzi, hogy az eredményül kapott frissített tulajdonost vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="3469e-116">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3469e-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3469e-117">-Path</span></span>
<span data-ttu-id="3469e-118">A módosítani kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="3469e-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3469e-119">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="3469e-119">-Type</span></span>
<span data-ttu-id="3469e-120">A beállítani kívánt tulajdonos típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3469e-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="3469e-121">A paraméter elfogadható értékei a következők: felhasználó és csoport.</span><span class="sxs-lookup"><span data-stu-id="3469e-121">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="3469e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3469e-122">-Confirm</span></span>
<span data-ttu-id="3469e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3469e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3469e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3469e-124">-WhatIf</span></span>
<span data-ttu-id="3469e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3469e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3469e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3469e-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3469e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3469e-127">-DefaultProfile</span></span>
<span data-ttu-id="3469e-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3469e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3469e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3469e-129">CommonParameters</span></span>
<span data-ttu-id="3469e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3469e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3469e-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3469e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3469e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3469e-132">INPUTS</span></span>

## <span data-ttu-id="3469e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3469e-133">OUTPUTS</span></span>

### <span data-ttu-id="3469e-134">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="3469e-134">string</span></span>
<span data-ttu-id="3469e-135">Ha a PassThru meg van adva, a frissített tulajdonost adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3469e-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="3469e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3469e-136">NOTES</span></span>

## <span data-ttu-id="3469e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3469e-137">RELATED LINKS</span></span>

[<span data-ttu-id="3469e-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="3469e-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


