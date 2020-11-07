---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f59796a51ccd1f3e5e77442cde434ab803d0781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837707"
---
# <span data-ttu-id="42dfd-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="42dfd-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="42dfd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="42dfd-103">Azure NetApp-fájlok (ANF) fiókjának törlése</span><span class="sxs-lookup"><span data-stu-id="42dfd-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="42dfd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42dfd-104">SYNTAX</span></span>

### <span data-ttu-id="42dfd-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42dfd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42dfd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42dfd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42dfd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42dfd-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dfd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="42dfd-109">A **Remove-AzNetAppFilesAccount** parancsmag törli az ANF-fiókját.</span><span class="sxs-lookup"><span data-stu-id="42dfd-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="42dfd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="42dfd-110">EXAMPLES</span></span>

### <span data-ttu-id="42dfd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42dfd-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="42dfd-112">Ez a parancs törli a "MyAnfAccount" ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="42dfd-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="42dfd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42dfd-113">PARAMETERS</span></span>

### <span data-ttu-id="42dfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dfd-114">-DefaultProfile</span></span>
<span data-ttu-id="42dfd-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42dfd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dfd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42dfd-116">-InputObject</span></span>
<span data-ttu-id="42dfd-117">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="42dfd-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42dfd-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42dfd-118">-Name</span></span>
<span data-ttu-id="42dfd-119">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="42dfd-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dfd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42dfd-120">-PassThru</span></span>
<span data-ttu-id="42dfd-121">A megadott fiók sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="42dfd-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="42dfd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dfd-122">-ResourceGroupName</span></span>
<span data-ttu-id="42dfd-123">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="42dfd-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dfd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42dfd-124">-ResourceId</span></span>
<span data-ttu-id="42dfd-125">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="42dfd-125">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dfd-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42dfd-126">-Confirm</span></span>
<span data-ttu-id="42dfd-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42dfd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42dfd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dfd-128">-WhatIf</span></span>
<span data-ttu-id="42dfd-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42dfd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dfd-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42dfd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42dfd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dfd-131">CommonParameters</span></span>
<span data-ttu-id="42dfd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42dfd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="42dfd-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dfd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dfd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42dfd-134">INPUTS</span></span>

### <span data-ttu-id="42dfd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42dfd-135">System.String</span></span>

### <span data-ttu-id="42dfd-136">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="42dfd-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="42dfd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42dfd-137">OUTPUTS</span></span>

### <span data-ttu-id="42dfd-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42dfd-138">System.Boolean</span></span>

## <span data-ttu-id="42dfd-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42dfd-139">NOTES</span></span>

## <span data-ttu-id="42dfd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42dfd-140">RELATED LINKS</span></span>
