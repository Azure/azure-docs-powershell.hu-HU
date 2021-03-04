---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 2b4b225ca050e3efedb1de1371006a4ffdb87587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918953"
---
# <span data-ttu-id="fb3f9-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="fb3f9-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="fb3f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3f9-103">Megkísérli engedélyezni egy felhasználó által felügyelt kulcstárolónak a megadott Data Lake Store-fiók titkosítását.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="fb3f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb3f9-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3f9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb3f9-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3f9-106">Az **Enable-AzDataLakeStoreKeyVault** parancsmag megkísérli engedélyezni a felhasználó által felügyelt kulcstárolónak a megadott Data Lake Store-fiók titkosítását.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="fb3f9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb3f9-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3f9-108">1. példa: A ContosoADLS-fiók kulcstárának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fb3f9-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="fb3f9-109">Ez a parancs megkísérli engedélyezni a felhasználó által felügyelt kulcstárolót a ContosoADLS nevű Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="fb3f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb3f9-110">PARAMETERS</span></span>

### <span data-ttu-id="fb3f9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fb3f9-111">-Account</span></span>
<span data-ttu-id="fb3f9-112">The Data Lake Store account to enable the user managed Key Vault for</span><span class="sxs-lookup"><span data-stu-id="fb3f9-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3f9-113">-DefaultProfile</span></span>
<span data-ttu-id="fb3f9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb3f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb3f9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3f9-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb3f9-116">A fiókkal társított erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="fb3f9-117">Ha nincs megadva, a rendszer megpróbálja felderítni.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f9-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb3f9-118">-Confirm</span></span>
<span data-ttu-id="fb3f9-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3f9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3f9-120">-WhatIf</span></span>
<span data-ttu-id="fb3f9-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb3f9-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3f9-123">CommonParameters</span></span>
<span data-ttu-id="fb3f9-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3f9-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3f9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3f9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb3f9-126">INPUTS</span></span>

### <span data-ttu-id="fb3f9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fb3f9-127">System.String</span></span>

## <span data-ttu-id="fb3f9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb3f9-128">OUTPUTS</span></span>

### <span data-ttu-id="fb3f9-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="fb3f9-129">System.Void</span></span>

## <span data-ttu-id="fb3f9-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb3f9-130">NOTES</span></span>

## <span data-ttu-id="fb3f9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb3f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb3f9-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fb3f9-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="fb3f9-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fb3f9-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

