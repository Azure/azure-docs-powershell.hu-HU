---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679483"
---
# <span data-ttu-id="604a8-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="604a8-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="604a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="604a8-102">SYNOPSIS</span></span>
<span data-ttu-id="604a8-103">Az adattó-elemzés titkának törlése</span><span class="sxs-lookup"><span data-stu-id="604a8-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="604a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="604a8-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="604a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="604a8-105">DESCRIPTION</span></span>
<span data-ttu-id="604a8-106">A **Remove-AzureRmDataLakeAnalyticsCatalogSecret** parancsmag az Azure Data-tó Analytics-katalógusának titkát törli.</span><span class="sxs-lookup"><span data-stu-id="604a8-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="604a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="604a8-107">EXAMPLES</span></span>

### <span data-ttu-id="604a8-108">1. példa: titkos kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="604a8-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="604a8-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-katalógus titkát.</span><span class="sxs-lookup"><span data-stu-id="604a8-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="604a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="604a8-110">PARAMETERS</span></span>

### <span data-ttu-id="604a8-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="604a8-111">-Account</span></span>
<span data-ttu-id="604a8-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="604a8-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="604a8-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="604a8-113">-DatabaseName</span></span>
<span data-ttu-id="604a8-114">A titkot birtokló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="604a8-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="604a8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="604a8-115">-Force</span></span>
<span data-ttu-id="604a8-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="604a8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="604a8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="604a8-117">-Name</span></span>
<span data-ttu-id="604a8-118">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="604a8-118">Specifies the name of the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604a8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="604a8-119">-PassThru</span></span>
<span data-ttu-id="604a8-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="604a8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="604a8-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="604a8-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604a8-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="604a8-122">-Confirm</span></span>
<span data-ttu-id="604a8-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="604a8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604a8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604a8-124">-WhatIf</span></span>
<span data-ttu-id="604a8-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="604a8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="604a8-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="604a8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604a8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604a8-127">-DefaultProfile</span></span>
<span data-ttu-id="604a8-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="604a8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="604a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604a8-129">CommonParameters</span></span>
<span data-ttu-id="604a8-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="604a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604a8-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604a8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604a8-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="604a8-132">INPUTS</span></span>

## <span data-ttu-id="604a8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="604a8-133">OUTPUTS</span></span>

### <span data-ttu-id="604a8-134">bool</span><span class="sxs-lookup"><span data-stu-id="604a8-134">bool</span></span>
<span data-ttu-id="604a8-135">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="604a8-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="604a8-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="604a8-136">NOTES</span></span>

## <span data-ttu-id="604a8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="604a8-137">RELATED LINKS</span></span>

[<span data-ttu-id="604a8-138">Új – AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="604a8-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="604a8-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="604a8-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


