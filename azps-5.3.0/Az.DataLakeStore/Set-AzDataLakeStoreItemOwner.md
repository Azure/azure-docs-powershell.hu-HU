---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465785"
---
# <span data-ttu-id="18266-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="18266-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="18266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18266-102">SYNOPSIS</span></span>
<span data-ttu-id="18266-103">Módosítja egy adattavatárban lévő fájl vagy mappa tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="18266-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="18266-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18266-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18266-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18266-105">DESCRIPTION</span></span>
<span data-ttu-id="18266-106">A **Set-AzDataLakeStoreItemOwner** parancsmag módosítja a Data Lake Store-ban található fájl vagy mappa tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="18266-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="18266-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18266-107">EXAMPLES</span></span>

### <span data-ttu-id="18266-108">1. példa: Elem tulajdonosának beállítása</span><span class="sxs-lookup"><span data-stu-id="18266-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="18266-109">Ez a parancs Patti Fullerre állítja a gyökérkönyvtár tulajdonosát.</span><span class="sxs-lookup"><span data-stu-id="18266-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="18266-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18266-110">PARAMETERS</span></span>

### <span data-ttu-id="18266-111">-Account</span><span class="sxs-lookup"><span data-stu-id="18266-111">-Account</span></span>
<span data-ttu-id="18266-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18266-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="18266-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18266-113">-DefaultProfile</span></span>
<span data-ttu-id="18266-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18266-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18266-115">-Id</span><span class="sxs-lookup"><span data-stu-id="18266-115">-Id</span></span>
<span data-ttu-id="18266-116">Annak az AzureActive Directory-felhasználónak, csoportnak vagy szolgáltatásnévnek az objektumazonosítóját adja meg, amely a tulajdonosként használható.</span><span class="sxs-lookup"><span data-stu-id="18266-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="18266-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18266-117">-PassThru</span></span>
<span data-ttu-id="18266-118">Azt jelzi, hogy az eredményül kapott frissített tulajdonost kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="18266-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="18266-119">-Path</span><span class="sxs-lookup"><span data-stu-id="18266-119">-Path</span></span>
<span data-ttu-id="18266-120">A módosítani kívánt elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="18266-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="18266-121">-Type</span><span class="sxs-lookup"><span data-stu-id="18266-121">-Type</span></span>
<span data-ttu-id="18266-122">A beállított tulajdonos típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="18266-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="18266-123">A paraméter elfogadható értékei a következőek: Felhasználó és Csoport.</span><span class="sxs-lookup"><span data-stu-id="18266-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="18266-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18266-124">-Confirm</span></span>
<span data-ttu-id="18266-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18266-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18266-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18266-126">-WhatIf</span></span>
<span data-ttu-id="18266-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18266-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18266-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18266-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18266-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18266-129">CommonParameters</span></span>
<span data-ttu-id="18266-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18266-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18266-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18266-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18266-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18266-132">INPUTS</span></span>

### <span data-ttu-id="18266-133">System.String</span><span class="sxs-lookup"><span data-stu-id="18266-133">System.String</span></span>

### <span data-ttu-id="18266-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="18266-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="18266-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="18266-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="18266-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="18266-136">System.Guid</span></span>

### <span data-ttu-id="18266-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18266-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18266-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18266-138">OUTPUTS</span></span>

### <span data-ttu-id="18266-139">System.String</span><span class="sxs-lookup"><span data-stu-id="18266-139">System.String</span></span>

## <span data-ttu-id="18266-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18266-140">NOTES</span></span>

## <span data-ttu-id="18266-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18266-141">RELATED LINKS</span></span>

[<span data-ttu-id="18266-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="18266-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


