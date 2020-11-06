---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493531"
---
# <span data-ttu-id="962bf-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="962bf-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="962bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="962bf-102">SYNOPSIS</span></span>
<span data-ttu-id="962bf-103">Az Azure Data Lake Analytics hitelesítő adatainak törlése</span><span class="sxs-lookup"><span data-stu-id="962bf-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="962bf-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="962bf-105">DESCRIPTION</span></span>
<span data-ttu-id="962bf-106">Az Remove-AzureRmDataLakeAnalyticsCatalogCredential parancsmag törli az Azure Data Lake Analytics katalógusának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="962bf-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="962bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="962bf-107">EXAMPLES</span></span>

### <span data-ttu-id="962bf-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="962bf-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="962bf-109">Ez a parancs eltávolítja a megadott adattó-Analytics-katalógus hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="962bf-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="962bf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="962bf-110">PARAMETERS</span></span>

### <span data-ttu-id="962bf-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="962bf-111">-Account</span></span>
<span data-ttu-id="962bf-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="962bf-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="962bf-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="962bf-113">-DatabaseName</span></span>
<span data-ttu-id="962bf-114">A hitelesítő adatokat tároló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="962bf-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="962bf-115">-Force</span></span>
<span data-ttu-id="962bf-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="962bf-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="962bf-117">-Name</span></span>
<span data-ttu-id="962bf-118">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="962bf-118">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="962bf-119">-PassThru</span></span>
<span data-ttu-id="962bf-120">Azt jelzi, hogy ez a parancsmag nem várja meg, amíg a művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="962bf-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="962bf-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="962bf-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="962bf-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="962bf-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-123">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="962bf-123">-Password</span></span>
<span data-ttu-id="962bf-124">A hitelesítő adatok jelszava.</span><span class="sxs-lookup"><span data-stu-id="962bf-124">The password for the credential.</span></span>
<span data-ttu-id="962bf-125">Erre akkor van szükség, ha a hívó nem a fiók tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="962bf-125">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-126">-Recurse</span><span class="sxs-lookup"><span data-stu-id="962bf-126">-Recurse</span></span>
<span data-ttu-id="962bf-127">Azt jelzi, hogy a törlési műveletnek végig kell haladnia, és a hitelesítő adatoktól függő minden erőforrást törölnie kell.</span><span class="sxs-lookup"><span data-stu-id="962bf-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="962bf-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="962bf-128">-Confirm</span></span>
<span data-ttu-id="962bf-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="962bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962bf-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962bf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962bf-131">-DefaultProfile</span></span>
<span data-ttu-id="962bf-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="962bf-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962bf-133">CommonParameters</span></span>
<span data-ttu-id="962bf-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="962bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962bf-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962bf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962bf-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="962bf-136">INPUTS</span></span>

## <span data-ttu-id="962bf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="962bf-137">OUTPUTS</span></span>

### <span data-ttu-id="962bf-138">bool</span><span class="sxs-lookup"><span data-stu-id="962bf-138">bool</span></span>
<span data-ttu-id="962bf-139">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="962bf-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="962bf-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="962bf-140">NOTES</span></span>

## <span data-ttu-id="962bf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="962bf-141">RELATED LINKS</span></span>

