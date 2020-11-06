---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: aa7dace3141210e8c4ff6055a011f34523c5b586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494076"
---
# <span data-ttu-id="fb52d-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="fb52d-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="fb52d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb52d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb52d-103">Az adattó-elemzés titkának törlése</span><span class="sxs-lookup"><span data-stu-id="fb52d-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb52d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb52d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb52d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb52d-105">DESCRIPTION</span></span>
<span data-ttu-id="fb52d-106">A **Remove-AzureRmDataLakeAnalyticsCatalogSecret** parancsmag az Azure Data-tó Analytics-katalógusának titkát törli.</span><span class="sxs-lookup"><span data-stu-id="fb52d-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="fb52d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb52d-107">EXAMPLES</span></span>

### <span data-ttu-id="fb52d-108">1. példa: titkos kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fb52d-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="fb52d-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-katalógus titkát.</span><span class="sxs-lookup"><span data-stu-id="fb52d-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="fb52d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb52d-110">PARAMETERS</span></span>

### <span data-ttu-id="fb52d-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fb52d-111">-Account</span></span>
<span data-ttu-id="fb52d-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb52d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fb52d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb52d-113">-DatabaseName</span></span>
<span data-ttu-id="fb52d-114">A titkot birtokló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb52d-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="fb52d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb52d-115">-DefaultProfile</span></span>
<span data-ttu-id="fb52d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb52d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb52d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fb52d-117">-Force</span></span>
<span data-ttu-id="fb52d-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fb52d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb52d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb52d-119">-Name</span></span>
<span data-ttu-id="fb52d-120">A titok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb52d-120">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="fb52d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb52d-121">-PassThru</span></span>
<span data-ttu-id="fb52d-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fb52d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb52d-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fb52d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb52d-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb52d-124">-Confirm</span></span>
<span data-ttu-id="fb52d-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb52d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb52d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb52d-126">-WhatIf</span></span>
<span data-ttu-id="fb52d-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb52d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb52d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb52d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb52d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb52d-129">CommonParameters</span></span>
<span data-ttu-id="fb52d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb52d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb52d-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb52d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb52d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb52d-132">INPUTS</span></span>

### <span data-ttu-id="fb52d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fb52d-133">System.String</span></span>

## <span data-ttu-id="fb52d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb52d-134">OUTPUTS</span></span>

### <span data-ttu-id="fb52d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb52d-135">System.Boolean</span></span>

## <span data-ttu-id="fb52d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb52d-136">NOTES</span></span>

## <span data-ttu-id="fb52d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb52d-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb52d-138">Új – AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="fb52d-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="fb52d-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="fb52d-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


