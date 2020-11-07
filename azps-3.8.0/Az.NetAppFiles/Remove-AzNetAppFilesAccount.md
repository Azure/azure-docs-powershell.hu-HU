---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: de0f71a91ec4445ae4be58e904e58eb3a97cb9a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845037"
---
# <span data-ttu-id="7cb0c-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7cb0c-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7cb0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb0c-103">Azure NetApp-fájlok (ANF) fiókjának törlése</span><span class="sxs-lookup"><span data-stu-id="7cb0c-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="7cb0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cb0c-104">SYNTAX</span></span>

### <span data-ttu-id="7cb0c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cb0c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb0c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb0c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cb0c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb0c-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb0c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cb0c-108">DESCRIPTION</span></span>
<span data-ttu-id="7cb0c-109">A **Remove-AzNetAppFilesAccount** parancsmag törli az ANF-fiókját.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="7cb0c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7cb0c-110">EXAMPLES</span></span>

### <span data-ttu-id="7cb0c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7cb0c-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="7cb0c-112">Ez a parancs törli a "MyAnfAccount" ANF-fiókot.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="7cb0c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cb0c-113">PARAMETERS</span></span>

### <span data-ttu-id="7cb0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb0c-114">-DefaultProfile</span></span>
<span data-ttu-id="7cb0c-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb0c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb0c-116">-InputObject</span></span>
<span data-ttu-id="7cb0c-117">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="7cb0c-117">The account object to remove</span></span>

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

### <span data-ttu-id="7cb0c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cb0c-118">-Name</span></span>
<span data-ttu-id="7cb0c-119">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="7cb0c-119">The name of the ANF account</span></span>

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

### <span data-ttu-id="7cb0c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cb0c-120">-PassThru</span></span>
<span data-ttu-id="7cb0c-121">A megadott fiók sikeres eltávolításának visszaadása</span><span class="sxs-lookup"><span data-stu-id="7cb0c-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="7cb0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7cb0c-123">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="7cb0c-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7cb0c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cb0c-124">-ResourceId</span></span>
<span data-ttu-id="7cb0c-125">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7cb0c-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="7cb0c-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cb0c-126">-Confirm</span></span>
<span data-ttu-id="7cb0c-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb0c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb0c-128">-WhatIf</span></span>
<span data-ttu-id="7cb0c-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb0c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb0c-131">CommonParameters</span></span>
<span data-ttu-id="7cb0c-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cb0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7cb0c-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb0c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb0c-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cb0c-134">INPUTS</span></span>

### <span data-ttu-id="7cb0c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7cb0c-135">System.String</span></span>

### <span data-ttu-id="7cb0c-136">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7cb0c-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7cb0c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cb0c-137">OUTPUTS</span></span>

### <span data-ttu-id="7cb0c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cb0c-138">System.Boolean</span></span>

## <span data-ttu-id="7cb0c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cb0c-139">NOTES</span></span>

## <span data-ttu-id="7cb0c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cb0c-140">RELATED LINKS</span></span>
