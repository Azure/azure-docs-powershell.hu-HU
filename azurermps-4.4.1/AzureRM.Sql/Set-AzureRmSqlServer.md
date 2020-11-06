---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494599"
---
# <span data-ttu-id="00274-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="00274-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="00274-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00274-102">SYNOPSIS</span></span>
<span data-ttu-id="00274-103">SQL-adatbázis kiszolgálójának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="00274-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00274-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00274-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00274-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00274-105">DESCRIPTION</span></span>
<span data-ttu-id="00274-106">A **set-AzureRmSqlServer** parancsmag egy Azure SQL-adatbázis kiszolgálójának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="00274-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="00274-107">Példák</span><span class="sxs-lookup"><span data-stu-id="00274-107">EXAMPLES</span></span>

### <span data-ttu-id="00274-108">1. példa: a rendszergazdai jelszó alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="00274-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="00274-109">Ez a parancs a server01 nevű AzureSQL-kiszolgálón visszaállítja a rendszergazdai jelszót.</span><span class="sxs-lookup"><span data-stu-id="00274-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="00274-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00274-110">PARAMETERS</span></span>

### <span data-ttu-id="00274-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="00274-111">-AssignIdentity</span></span>
<span data-ttu-id="00274-112">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="00274-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="00274-113">-Force</span><span class="sxs-lookup"><span data-stu-id="00274-113">-Force</span></span>
<span data-ttu-id="00274-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="00274-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00274-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00274-115">-ResourceGroupName</span></span>
<span data-ttu-id="00274-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="00274-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="00274-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="00274-117">-ServerName</span></span>
<span data-ttu-id="00274-118">Itt adhatja meg annak a kiszolgálónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="00274-118">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00274-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="00274-119">-ServerVersion</span></span>
<span data-ttu-id="00274-120">Annak a verziónak a verziószáma, amelyre a parancsmag a kiszolgálót módosítja.</span><span class="sxs-lookup"><span data-stu-id="00274-120">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="00274-121">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="00274-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00274-122">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="00274-122">-SqlAdministratorPassword</span></span>
<span data-ttu-id="00274-123">Új jelszót ad meg **SecureString** az adatbázis-kiszolgáló rendszergazdájához.</span><span class="sxs-lookup"><span data-stu-id="00274-123">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="00274-124">Ha **SecureString** szeretne beolvasni, használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="00274-124">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="00274-125">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="00274-125">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00274-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="00274-126">-Tags</span></span>
<span data-ttu-id="00274-127">A parancsmag által a kiszolgálóhoz társított címkék szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="00274-127">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="00274-128">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="00274-128">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="00274-129">Példa:</span><span class="sxs-lookup"><span data-stu-id="00274-129">For example:</span></span>

<span data-ttu-id="00274-130">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="00274-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00274-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00274-131">-Confirm</span></span>
<span data-ttu-id="00274-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00274-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00274-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00274-133">-WhatIf</span></span>
<span data-ttu-id="00274-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00274-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00274-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00274-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00274-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00274-136">-DefaultProfile</span></span>
<span data-ttu-id="00274-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00274-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00274-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00274-138">CommonParameters</span></span>
<span data-ttu-id="00274-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00274-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00274-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00274-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00274-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00274-141">INPUTS</span></span>

## <span data-ttu-id="00274-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00274-142">OUTPUTS</span></span>

### <span data-ttu-id="00274-143">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="00274-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="00274-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00274-144">NOTES</span></span>

## <span data-ttu-id="00274-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00274-145">RELATED LINKS</span></span>

[<span data-ttu-id="00274-146">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="00274-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
