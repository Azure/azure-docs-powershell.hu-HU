---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: af6acce52ee41297e650abb76188324ecf313679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494523"
---
# <span data-ttu-id="8e056-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="8e056-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="8e056-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e056-102">SYNOPSIS</span></span>
<span data-ttu-id="8e056-103">Az Azure Data Lake Analytics hitelesítő adatainak törlése</span><span class="sxs-lookup"><span data-stu-id="8e056-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e056-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e056-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e056-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e056-105">DESCRIPTION</span></span>
<span data-ttu-id="8e056-106">Az Remove-AzureRmDataLakeAnalyticsCatalogCredential parancsmag törli az Azure Data Lake Analytics katalógusának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="8e056-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="8e056-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e056-107">EXAMPLES</span></span>

### <span data-ttu-id="8e056-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8e056-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="8e056-109">Ez a parancs eltávolítja a megadott adattó-Analytics-katalógus hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="8e056-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="8e056-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e056-110">PARAMETERS</span></span>

### <span data-ttu-id="8e056-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8e056-111">-Account</span></span>
<span data-ttu-id="8e056-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e056-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e056-113">-DatabaseName</span></span>
<span data-ttu-id="8e056-114">A hitelesítő adatokat tároló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e056-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e056-115">-DefaultProfile</span></span>
<span data-ttu-id="8e056-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e056-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8e056-117">-Force</span></span>
<span data-ttu-id="8e056-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8e056-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e056-119">-Name</span></span>
<span data-ttu-id="8e056-120">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e056-120">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e056-121">-PassThru</span></span>
<span data-ttu-id="8e056-122">Azt jelzi, hogy ez a parancsmag nem várja meg, amíg a művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="8e056-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="8e056-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8e056-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8e056-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8e056-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-125">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="8e056-125">-Password</span></span>
<span data-ttu-id="8e056-126">A hitelesítő adatok jelszava.</span><span class="sxs-lookup"><span data-stu-id="8e056-126">The password for the credential.</span></span>
<span data-ttu-id="8e056-127">Erre akkor van szükség, ha a hívó nem a fiók tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="8e056-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="8e056-128">-Recurse</span></span>
<span data-ttu-id="8e056-129">Azt jelzi, hogy a törlési műveletnek végig kell haladnia, és a hitelesítő adatoktól függő minden erőforrást törölnie kell.</span><span class="sxs-lookup"><span data-stu-id="8e056-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e056-130">-Confirm</span></span>
<span data-ttu-id="8e056-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e056-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e056-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e056-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e056-133">CommonParameters</span></span>
<span data-ttu-id="8e056-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e056-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e056-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e056-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e056-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e056-136">INPUTS</span></span>

### <span data-ttu-id="8e056-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e056-137">None</span></span>
<span data-ttu-id="8e056-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8e056-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e056-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e056-139">OUTPUTS</span></span>

### <span data-ttu-id="8e056-140">bool</span><span class="sxs-lookup"><span data-stu-id="8e056-140">bool</span></span>
<span data-ttu-id="8e056-141">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8e056-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="8e056-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e056-142">NOTES</span></span>

## <span data-ttu-id="8e056-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e056-143">RELATED LINKS</span></span>

