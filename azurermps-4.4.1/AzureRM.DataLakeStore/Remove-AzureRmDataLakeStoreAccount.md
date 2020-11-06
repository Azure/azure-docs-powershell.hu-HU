---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500859"
---
# <span data-ttu-id="ce5fa-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce5fa-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="ce5fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ce5fa-103">Véglegesen törli az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce5fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce5fa-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce5fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ce5fa-106">A **Remove-AzureRmDataLakeStoreAccount** parancsmag véglegesen törli az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="ce5fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ce5fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ce5fa-108">1. példa: az adattó áruházbeli fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ce5fa-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="ce5fa-109">Ez a parancs eltávolítja a ContosoADL nevű fiókot az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="ce5fa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce5fa-110">PARAMETERS</span></span>

### <span data-ttu-id="ce5fa-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ce5fa-111">-Force</span></span>
<span data-ttu-id="ce5fa-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce5fa-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce5fa-113">-Name</span></span>
<span data-ttu-id="ce5fa-114">Az eltávolítandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="ce5fa-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce5fa-115">-PassThru</span></span>
<span data-ttu-id="ce5fa-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce5fa-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce5fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce5fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce5fa-119">Azt az erőforráscsoportot adja meg, amely az eltávolítandó fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="ce5fa-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce5fa-120">-Confirm</span></span>
<span data-ttu-id="ce5fa-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce5fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce5fa-122">-WhatIf</span></span>
<span data-ttu-id="ce5fa-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce5fa-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce5fa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce5fa-125">-DefaultProfile</span></span>
<span data-ttu-id="ce5fa-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce5fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce5fa-127">CommonParameters</span></span>
<span data-ttu-id="ce5fa-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce5fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce5fa-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce5fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce5fa-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce5fa-130">INPUTS</span></span>

## <span data-ttu-id="ce5fa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce5fa-131">OUTPUTS</span></span>

### <span data-ttu-id="ce5fa-132">bool</span><span class="sxs-lookup"><span data-stu-id="ce5fa-132">bool</span></span>
<span data-ttu-id="ce5fa-133">Ha a PassThru meg van adva, akkor a sikeres befejezéshez az igaz értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ce5fa-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="ce5fa-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce5fa-134">NOTES</span></span>

## <span data-ttu-id="ce5fa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce5fa-135">RELATED LINKS</span></span>

[<span data-ttu-id="ce5fa-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce5fa-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ce5fa-137">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce5fa-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ce5fa-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce5fa-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ce5fa-139">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ce5fa-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


