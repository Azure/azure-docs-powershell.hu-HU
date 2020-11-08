---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010830"
---
# <span data-ttu-id="9735c-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="9735c-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="9735c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9735c-102">SYNOPSIS</span></span>
<span data-ttu-id="9735c-103">Az Azure Data Lake Analytics hitelesítő adatainak törlése</span><span class="sxs-lookup"><span data-stu-id="9735c-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="9735c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9735c-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9735c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9735c-105">DESCRIPTION</span></span>
<span data-ttu-id="9735c-106">Az Remove-AzDataLakeAnalyticsCatalogCredential parancsmag törli az Azure Data Lake Analytics katalógusának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9735c-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="9735c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9735c-107">EXAMPLES</span></span>

### <span data-ttu-id="9735c-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9735c-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="9735c-109">Ez a parancs eltávolítja a megadott adattó-Analytics-katalógus hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9735c-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="9735c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9735c-110">PARAMETERS</span></span>

### <span data-ttu-id="9735c-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9735c-111">-Account</span></span>
<span data-ttu-id="9735c-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9735c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9735c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9735c-113">-DatabaseName</span></span>
<span data-ttu-id="9735c-114">A hitelesítő adatokat tároló adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9735c-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="9735c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9735c-115">-DefaultProfile</span></span>
<span data-ttu-id="9735c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9735c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9735c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9735c-117">-Force</span></span>
<span data-ttu-id="9735c-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9735c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9735c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9735c-119">-Name</span></span>
<span data-ttu-id="9735c-120">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9735c-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="9735c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9735c-121">-PassThru</span></span>
<span data-ttu-id="9735c-122">Azt jelzi, hogy ez a parancsmag nem várja meg, amíg a művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="9735c-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="9735c-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9735c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9735c-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9735c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9735c-125">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="9735c-125">-Password</span></span>
<span data-ttu-id="9735c-126">A hitelesítő adatok jelszava.</span><span class="sxs-lookup"><span data-stu-id="9735c-126">The password for the credential.</span></span>
<span data-ttu-id="9735c-127">Erre akkor van szükség, ha a hívó nem a fiók tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="9735c-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="9735c-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9735c-128">-Recurse</span></span>
<span data-ttu-id="9735c-129">Azt jelzi, hogy a törlési műveletnek végig kell haladnia, és a hitelesítő adatoktól függő minden erőforrást törölnie kell.</span><span class="sxs-lookup"><span data-stu-id="9735c-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="9735c-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9735c-130">-Confirm</span></span>
<span data-ttu-id="9735c-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9735c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9735c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9735c-132">-WhatIf</span></span>
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

### <span data-ttu-id="9735c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9735c-133">CommonParameters</span></span>
<span data-ttu-id="9735c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9735c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9735c-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9735c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9735c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9735c-136">INPUTS</span></span>

### <span data-ttu-id="9735c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9735c-137">System.String</span></span>

### <span data-ttu-id="9735c-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9735c-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="9735c-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9735c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9735c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9735c-140">OUTPUTS</span></span>

### <span data-ttu-id="9735c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9735c-141">System.Boolean</span></span>

## <span data-ttu-id="9735c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9735c-142">NOTES</span></span>

## <span data-ttu-id="9735c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9735c-143">RELATED LINKS</span></span>
