---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 0e8adfc9ef5cfd5525a0e07b35c3eb1b918b9ba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666864"
---
# <span data-ttu-id="22c10-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="22c10-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="22c10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22c10-102">SYNOPSIS</span></span>
<span data-ttu-id="22c10-103">Megkísérli engedélyezni a felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="22c10-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="22c10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22c10-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22c10-105">DESCRIPTION</span></span>
<span data-ttu-id="22c10-106">Az **enable-AzDataLakeStoreKeyVault** parancsmag megkísérli engedélyezni egy felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="22c10-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="22c10-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22c10-107">EXAMPLES</span></span>

### <span data-ttu-id="22c10-108">1. példa: a ContosoADLS-fiók fő boltozatának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="22c10-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="22c10-109">A parancs megkísérli engedélyezni a ContosoADLS nevű adattó-tároló fiók felhasználó által felügyelt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="22c10-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="22c10-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22c10-110">PARAMETERS</span></span>

### <span data-ttu-id="22c10-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="22c10-111">-Account</span></span>
<span data-ttu-id="22c10-112">Az adattó-tároló fiók a felhasználó által felügyelt kulcs boltozatának engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="22c10-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="22c10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c10-113">-DefaultProfile</span></span>
<span data-ttu-id="22c10-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22c10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22c10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c10-115">-ResourceGroupName</span></span>
<span data-ttu-id="22c10-116">A fiókhoz társított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="22c10-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="22c10-117">Ha a program nem adja meg, a program megpróbálja észlelni a lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="22c10-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="22c10-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22c10-118">-Confirm</span></span>
<span data-ttu-id="22c10-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22c10-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c10-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c10-120">-WhatIf</span></span>
<span data-ttu-id="22c10-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22c10-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22c10-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22c10-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c10-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c10-123">CommonParameters</span></span>
<span data-ttu-id="22c10-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22c10-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c10-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c10-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c10-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c10-126">INPUTS</span></span>

### <span data-ttu-id="22c10-127">System. String</span><span class="sxs-lookup"><span data-stu-id="22c10-127">System.String</span></span>

## <span data-ttu-id="22c10-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c10-128">OUTPUTS</span></span>

### <span data-ttu-id="22c10-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="22c10-129">System.Void</span></span>

## <span data-ttu-id="22c10-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22c10-130">NOTES</span></span>

## <span data-ttu-id="22c10-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22c10-131">RELATED LINKS</span></span>

[<span data-ttu-id="22c10-132">Új – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22c10-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="22c10-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22c10-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

