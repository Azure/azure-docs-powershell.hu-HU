---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144315"
---
# <span data-ttu-id="735a8-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="735a8-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="735a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735a8-102">SYNOPSIS</span></span>
<span data-ttu-id="735a8-103">A Data Lake Store-fiók végleges törlése.</span><span class="sxs-lookup"><span data-stu-id="735a8-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="735a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="735a8-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="735a8-105">DESCRIPTION</span></span>
<span data-ttu-id="735a8-106">A **Remove-AzDataLakeStoreAccount** parancsmag véglegesen töröl egy Data Lake Store-fiókot.</span><span class="sxs-lookup"><span data-stu-id="735a8-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="735a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="735a8-107">EXAMPLES</span></span>

### <span data-ttu-id="735a8-108">1. példa: Adattavatár-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="735a8-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="735a8-109">Ez a parancs eltávolítja a ContosoADL nevű fiókot az adattavas áruházból.</span><span class="sxs-lookup"><span data-stu-id="735a8-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="735a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="735a8-110">PARAMETERS</span></span>

### <span data-ttu-id="735a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735a8-111">-DefaultProfile</span></span>
<span data-ttu-id="735a8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="735a8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="735a8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="735a8-113">-Force</span></span>
<span data-ttu-id="735a8-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="735a8-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="735a8-115">-Name</span></span>
<span data-ttu-id="735a8-116">Az eltávolítható fiók neve.</span><span class="sxs-lookup"><span data-stu-id="735a8-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735a8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="735a8-117">-PassThru</span></span>
<span data-ttu-id="735a8-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="735a8-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="735a8-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="735a8-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="735a8-121">Az eltávolítható fiókot tartalmazó erőforráscsoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="735a8-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735a8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="735a8-122">-Confirm</span></span>
<span data-ttu-id="735a8-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="735a8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="735a8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735a8-124">-WhatIf</span></span>
<span data-ttu-id="735a8-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="735a8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="735a8-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="735a8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="735a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735a8-127">CommonParameters</span></span>
<span data-ttu-id="735a8-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735a8-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735a8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735a8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="735a8-130">INPUTS</span></span>

### <span data-ttu-id="735a8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="735a8-131">System.String</span></span>

## <span data-ttu-id="735a8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="735a8-132">OUTPUTS</span></span>

### <span data-ttu-id="735a8-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="735a8-133">System.Boolean</span></span>

## <span data-ttu-id="735a8-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="735a8-134">NOTES</span></span>

## <span data-ttu-id="735a8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="735a8-135">RELATED LINKS</span></span>

[<span data-ttu-id="735a8-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="735a8-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="735a8-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="735a8-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="735a8-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="735a8-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="735a8-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="735a8-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


