---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 5316a55e29acb8edc5bd102d118eb2bcc53c2c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499572"
---
# <span data-ttu-id="88341-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="88341-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="88341-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88341-102">SYNOPSIS</span></span>
<span data-ttu-id="88341-103">Megkísérli engedélyezni a felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="88341-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88341-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88341-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88341-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88341-105">DESCRIPTION</span></span>
<span data-ttu-id="88341-106">Az **enable-AzureRmDataLakeStoreKeyVault** parancsmag megkísérli engedélyezni egy felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="88341-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="88341-107">Példák</span><span class="sxs-lookup"><span data-stu-id="88341-107">EXAMPLES</span></span>

### <span data-ttu-id="88341-108">1. példa: a ContosoADLS-fiók fő boltozatának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="88341-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="88341-109">A parancs megkísérli engedélyezni a ContosoADLS nevű adattó-tároló fiók felhasználó által felügyelt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="88341-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="88341-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88341-110">PARAMETERS</span></span>

### <span data-ttu-id="88341-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="88341-111">-Account</span></span>
<span data-ttu-id="88341-112">Az adattó-tároló fiók a felhasználó által felügyelt kulcs boltozatának engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="88341-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="88341-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88341-113">-DefaultProfile</span></span>
<span data-ttu-id="88341-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="88341-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88341-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88341-115">-ResourceGroupName</span></span>
<span data-ttu-id="88341-116">A fiókhoz társított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="88341-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="88341-117">Ha a program nem adja meg, a program megpróbálja észlelni a lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="88341-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="88341-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88341-118">-Confirm</span></span>
<span data-ttu-id="88341-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88341-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88341-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88341-120">-WhatIf</span></span>
<span data-ttu-id="88341-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88341-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88341-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88341-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88341-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88341-123">CommonParameters</span></span>
<span data-ttu-id="88341-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88341-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88341-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88341-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88341-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88341-126">INPUTS</span></span>

### <span data-ttu-id="88341-127">System. String</span><span class="sxs-lookup"><span data-stu-id="88341-127">System.String</span></span>

## <span data-ttu-id="88341-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88341-128">OUTPUTS</span></span>

### <span data-ttu-id="88341-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="88341-129">System.Void</span></span>

## <span data-ttu-id="88341-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88341-130">NOTES</span></span>

## <span data-ttu-id="88341-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88341-131">RELATED LINKS</span></span>

[<span data-ttu-id="88341-132">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="88341-132">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="88341-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="88341-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

