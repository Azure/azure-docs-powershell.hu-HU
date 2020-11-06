---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 062df0ddadc3cc0cfb2e1f0ef9954454b08c4352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494520"
---
# <span data-ttu-id="fb473-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="fb473-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="fb473-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb473-102">SYNOPSIS</span></span>
<span data-ttu-id="fb473-103">Megkísérli engedélyezni a felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="fb473-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb473-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb473-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb473-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb473-105">DESCRIPTION</span></span>
<span data-ttu-id="fb473-106">Az **enable-AzureRmDataLakeStoreKeyVault** parancsmag megkísérli engedélyezni egy felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="fb473-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="fb473-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb473-107">EXAMPLES</span></span>

### <span data-ttu-id="fb473-108">1. példa: a ContosoADLS-fiók fő boltozatának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fb473-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="fb473-109">A parancs megkísérli engedélyezni a ContosoADLS nevű adattó-tároló fiók felhasználó által felügyelt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fb473-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="fb473-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb473-110">PARAMETERS</span></span>

### <span data-ttu-id="fb473-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fb473-111">-Account</span></span>
<span data-ttu-id="fb473-112">Az adattó-tároló fiók a felhasználó által felügyelt kulcs boltozatának engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="fb473-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb473-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb473-113">-DefaultProfile</span></span>
<span data-ttu-id="fb473-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb473-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb473-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb473-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb473-116">A fiókhoz társított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fb473-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="fb473-117">Ha a program nem adja meg, a program megpróbálja észlelni a lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="fb473-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb473-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb473-118">-Confirm</span></span>
<span data-ttu-id="fb473-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb473-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb473-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb473-120">-WhatIf</span></span>
<span data-ttu-id="fb473-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb473-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb473-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb473-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb473-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb473-123">CommonParameters</span></span>
<span data-ttu-id="fb473-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb473-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb473-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb473-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb473-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb473-126">INPUTS</span></span>

### <span data-ttu-id="fb473-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fb473-127">System.String</span></span>

## <span data-ttu-id="fb473-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb473-128">OUTPUTS</span></span>

## <span data-ttu-id="fb473-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb473-129">NOTES</span></span>

## <span data-ttu-id="fb473-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb473-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb473-131">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fb473-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="fb473-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fb473-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

