---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297833"
---
# <span data-ttu-id="9a5a8-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9a5a8-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="9a5a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5a8-103">Véglegesen törli az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="9a5a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a5a8-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a5a8-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5a8-106">A **Remove-AzDataLakeStoreAccount** parancsmag véglegesen törli az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="9a5a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a5a8-107">EXAMPLES</span></span>

### <span data-ttu-id="9a5a8-108">1. példa: az adattó áruházbeli fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9a5a8-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="9a5a8-109">Ez a parancs eltávolítja a ContosoADL nevű fiókot az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="9a5a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a5a8-110">PARAMETERS</span></span>

### <span data-ttu-id="9a5a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5a8-111">-DefaultProfile</span></span>
<span data-ttu-id="9a5a8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9a5a8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a5a8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9a5a8-113">-Force</span></span>
<span data-ttu-id="9a5a8-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9a5a8-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a5a8-115">-Name</span></span>
<span data-ttu-id="9a5a8-116">Az eltávolítandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="9a5a8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a5a8-117">-PassThru</span></span>
<span data-ttu-id="9a5a8-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a5a8-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a5a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="9a5a8-121">Azt az erőforráscsoportot adja meg, amely az eltávolítandó fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="9a5a8-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a5a8-122">-Confirm</span></span>
<span data-ttu-id="9a5a8-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5a8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5a8-124">-WhatIf</span></span>
<span data-ttu-id="9a5a8-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5a8-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a5a8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5a8-127">CommonParameters</span></span>
<span data-ttu-id="9a5a8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a5a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5a8-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5a8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5a8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a5a8-130">INPUTS</span></span>

### <span data-ttu-id="9a5a8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9a5a8-131">System.String</span></span>

## <span data-ttu-id="9a5a8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a5a8-132">OUTPUTS</span></span>

### <span data-ttu-id="9a5a8-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a5a8-133">System.Boolean</span></span>

## <span data-ttu-id="9a5a8-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a5a8-134">NOTES</span></span>

## <span data-ttu-id="9a5a8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a5a8-135">RELATED LINKS</span></span>

[<span data-ttu-id="9a5a8-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9a5a8-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9a5a8-137">Új – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9a5a8-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9a5a8-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9a5a8-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9a5a8-139">Teszt-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9a5a8-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


