---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 446bd86eb37e45d3b4b302fdedf46e1cbe05e51c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666802"
---
# <span data-ttu-id="52599-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="52599-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="52599-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52599-102">SYNOPSIS</span></span>
<span data-ttu-id="52599-103">Módosítja egy fájl vagy mappa tulajdonosát az adattó-áruházban.</span><span class="sxs-lookup"><span data-stu-id="52599-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52599-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52599-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52599-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="52599-105">DESCRIPTION</span></span>
<span data-ttu-id="52599-106">A **set-AzDataLakeStoreItemOwner** parancsmag módosította az adattó-tárolóban lévő fájlok vagy mappák tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="52599-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52599-107">Példák</span><span class="sxs-lookup"><span data-stu-id="52599-107">EXAMPLES</span></span>

### <span data-ttu-id="52599-108">Példa 1: egy elem tulajdonosának beállítása</span><span class="sxs-lookup"><span data-stu-id="52599-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="52599-109">Ez a parancs beállítja a gyökérkönyvtár tulajdonosát az Patti Fuller-nek.</span><span class="sxs-lookup"><span data-stu-id="52599-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="52599-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52599-110">PARAMETERS</span></span>

### <span data-ttu-id="52599-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="52599-111">-Account</span></span>
<span data-ttu-id="52599-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52599-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="52599-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52599-113">-DefaultProfile</span></span>
<span data-ttu-id="52599-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52599-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52599-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="52599-115">-Id</span></span>
<span data-ttu-id="52599-116">Itt adhatja meg a tulajdonosként használandó AzureActive-felhasználó,-csoport vagy-szolgáltató objektum-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="52599-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="52599-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52599-117">-PassThru</span></span>
<span data-ttu-id="52599-118">Jelzi, hogy az eredményül kapott frissített tulajdonost vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="52599-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="52599-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="52599-119">-Path</span></span>
<span data-ttu-id="52599-120">A módosítani kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="52599-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="52599-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="52599-121">-Type</span></span>
<span data-ttu-id="52599-122">A beállítani kívánt tulajdonos típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="52599-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="52599-123">A paraméter elfogadható értékei a következők: felhasználó és csoport.</span><span class="sxs-lookup"><span data-stu-id="52599-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="52599-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52599-124">-Confirm</span></span>
<span data-ttu-id="52599-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52599-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52599-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52599-126">-WhatIf</span></span>
<span data-ttu-id="52599-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52599-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52599-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52599-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52599-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52599-129">CommonParameters</span></span>
<span data-ttu-id="52599-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52599-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52599-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52599-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52599-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52599-132">INPUTS</span></span>

### <span data-ttu-id="52599-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52599-133">System.String</span></span>

### <span data-ttu-id="52599-134">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="52599-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="52599-135">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="52599-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="52599-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="52599-136">System.Guid</span></span>

### <span data-ttu-id="52599-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52599-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52599-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52599-138">OUTPUTS</span></span>

### <span data-ttu-id="52599-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52599-139">System.String</span></span>

## <span data-ttu-id="52599-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52599-140">NOTES</span></span>

## <span data-ttu-id="52599-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52599-141">RELATED LINKS</span></span>

[<span data-ttu-id="52599-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="52599-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


