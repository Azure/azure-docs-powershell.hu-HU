---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 6cc3b0f066f267b51a90c0cb0c56d1972ec92f5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668937"
---
# <span data-ttu-id="ec176-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ec176-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="ec176-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec176-102">SYNOPSIS</span></span>
<span data-ttu-id="ec176-103">Beolvassa az SQL Server fő központi kulcsait.</span><span class="sxs-lookup"><span data-stu-id="ec176-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="ec176-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec176-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec176-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec176-105">DESCRIPTION</span></span>
<span data-ttu-id="ec176-106">A Get-AzSqlServerKeyVaultKey parancsmag az SQL Server-kiszolgálók fő boltozati kulcsaival kapcsolatos információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ec176-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="ec176-107">Megtekintheti a kiszolgálók összes kulcsát, vagy megtekintheti az adott kulcsot a KeyId.</span><span class="sxs-lookup"><span data-stu-id="ec176-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="ec176-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ec176-108">EXAMPLES</span></span>

### <span data-ttu-id="ec176-109">1. példa: az összes kulcsos Vault-kulcs beolvasása</span><span class="sxs-lookup"><span data-stu-id="ec176-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ec176-110">Ez a parancs egy SQL Server-kiszolgálón beilleszti az összes kulcs boltozatos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ec176-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="ec176-111">ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típus: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 típus: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 ujjlenyomat: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="ec176-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="ec176-112">2. példa: adott kulcsos Vault-kulcs beszerzése</span><span class="sxs-lookup"><span data-stu-id="ec176-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ec176-113">Ez a parancs a Key Vault-kulcsot azonosító ' ' értékkel kapja https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 , majd a $MyServerKeyVaultKey változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ec176-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="ec176-114">A $MyServerKeyVaultKey tulajdonságait ellenőrizheti, hogy miként kaphat részleteket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="ec176-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="ec176-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec176-115">PARAMETERS</span></span>

### <span data-ttu-id="ec176-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec176-116">-DefaultProfile</span></span>
<span data-ttu-id="ec176-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ec176-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec176-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ec176-118">-KeyId</span></span>
<span data-ttu-id="ec176-119">Az Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="ec176-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="ec176-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec176-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec176-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ec176-121">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec176-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ec176-122">-ServerName</span></span>
<span data-ttu-id="ec176-123">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ec176-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ec176-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec176-124">-Confirm</span></span>
<span data-ttu-id="ec176-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec176-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec176-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec176-126">-WhatIf</span></span>
<span data-ttu-id="ec176-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec176-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec176-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec176-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec176-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec176-129">CommonParameters</span></span>
<span data-ttu-id="ec176-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec176-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec176-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ec176-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec176-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec176-132">INPUTS</span></span>

### <span data-ttu-id="ec176-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec176-133">System.String</span></span>

## <span data-ttu-id="ec176-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec176-134">OUTPUTS</span></span>

### <span data-ttu-id="ec176-135">Microsoft. Azure. Command. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="ec176-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="ec176-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec176-136">NOTES</span></span>

## <span data-ttu-id="ec176-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec176-137">RELATED LINKS</span></span>

[<span data-ttu-id="ec176-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ec176-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
