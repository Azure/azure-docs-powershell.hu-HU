---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: a168b48089052ed8daa764407254d04084ece771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493520"
---
# <span data-ttu-id="c7047-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7047-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="c7047-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7047-102">SYNOPSIS</span></span>
<span data-ttu-id="c7047-103">Megkísérli engedélyezni a felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="c7047-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7047-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7047-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7047-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7047-105">DESCRIPTION</span></span>
<span data-ttu-id="c7047-106">Az **enable-AzureRmDataLakeStoreKeyVault** parancsmag megkísérli engedélyezni egy felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.</span><span class="sxs-lookup"><span data-stu-id="c7047-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c7047-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7047-107">EXAMPLES</span></span>

### <span data-ttu-id="c7047-108">1. példa: a ContosoADLS-fiók fő boltozatának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="c7047-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="c7047-109">A parancs megkísérli engedélyezni a ContosoADLS nevű adattó-tároló fiók felhasználó által felügyelt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="c7047-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="c7047-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7047-110">PARAMETERS</span></span>

### <span data-ttu-id="c7047-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c7047-111">-Account</span></span>
<span data-ttu-id="c7047-112">Az adattó-tároló fiók a felhasználó által felügyelt kulcs boltozatának engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="c7047-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="c7047-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7047-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7047-114">A fiókhoz társított erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c7047-114">Name of resource group associated with the account.</span></span> <span data-ttu-id="c7047-115">Ha a program nem adja meg, a program megpróbálja észlelni a lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c7047-115">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="c7047-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7047-116">-Confirm</span></span>
<span data-ttu-id="c7047-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7047-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7047-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7047-118">-WhatIf</span></span>
<span data-ttu-id="c7047-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7047-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7047-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7047-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7047-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7047-121">-DefaultProfile</span></span>
<span data-ttu-id="c7047-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7047-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7047-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7047-123">CommonParameters</span></span>
<span data-ttu-id="c7047-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7047-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7047-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7047-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7047-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7047-126">INPUTS</span></span>

### <span data-ttu-id="c7047-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c7047-127">System.String</span></span>

## <span data-ttu-id="c7047-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7047-128">OUTPUTS</span></span>

## <span data-ttu-id="c7047-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7047-129">NOTES</span></span>

## <span data-ttu-id="c7047-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7047-130">RELATED LINKS</span></span>

[<span data-ttu-id="c7047-131">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c7047-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c7047-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c7047-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

